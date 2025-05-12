# 🎵 PacMusic - Demonstrasi CI/CD dengan GitHub Actions

PacMusic adalah proyek demonstrasi yang berfokus pada penerapan Continuous Integration (CI) dan Continuous Deployment (CD) menggunakan GitHub Actions, Docker, dan Git Secrets. Aplikasi web musik yang digunakan dalam proyek ini disediakan oleh bootcamp, dengan tujuan utama untuk mempelajari dan mendemonstrasikan alur kerja CI/CD.

## 🚀 Tujuan Proyek (Portofolio)

-   Mendemonstrasikan penerapan CI/CD menggunakan GitHub Actions untuk deployment ke AWS EC2.
-   Menunjukkan pemahaman tentang Docker untuk containerisasi dan Git Secrets untuk manajemen rahasia.
-   Menyediakan contoh alur kerja CI/CD untuk deployment ke lingkungan staging dan production.

## 🔧 Teknologi yang Digunakan

-   **CI/CD**: GitHub Actions
-   **Containerization**: Docker
-   **Cloud**: AWS EC2
-   **Manajemen Rahasia**: Git Secrets

## ⚙️ Alur Kerja CI/CD

### 1. Pengembangan dan Commit

-   Pengembang melakukan perubahan pada kode aplikasi.
-   Perubahan kode di-commit dan di-push ke repositori GitHub.

### 2. GitHub Actions: Build dan Test

-   Setiap kali ada push ke branch tertentu (misalnya, `main` atau `staging`), GitHub Actions secara otomatis melakukan:
    -   Build aplikasi (misalnya, membangun container Docker).
    -   Menjalankan pengujian otomatis (unit tests, integrasi tests, dll.).

### 3. GitHub Actions: Deployment ke Staging

-   Jika pengujian berhasil, GitHub Actions secara otomatis melakukan deployment aplikasi ke instance AWS EC2 staging.
-   Docker digunakan untuk memastikan konsistensi lingkungan.
-   Git Secrets digunakan untuk menyimpan kredensial AWS yang diperlukan untuk deployment.

### 4. Verifikasi di Staging

-   Setelah deployment ke staging, dilakukan verifikasi aplikasi.
-   Contoh verifikasi:
    -   Pengujian manual oleh pengembang.
    -   Pengujian otomatis tambahan.
    -   Dalam contoh proyek ini, verifikasi dilakukan dengan mengubah judul website untuk memastikan perubahan tercermin di lingkungan staging.

### 5. GitHub Actions: Deployment ke Production

-   Jika verifikasi di staging berhasil, GitHub Actions dapat dipicu (secara manual atau otomatis) untuk melakukan deployment aplikasi ke instance AWS EC2 production.
-   Proses deployment ke production mirip dengan deployment ke staging, menggunakan Docker dan Git Secrets.

### 6. Versioning/Releases

-   Setiap deployment ke production dapat dikaitkan dengan rilis (release) atau versi tertentu di GitHub.
-   Contoh: Dalam proyek ini, versi aplikasi di production diubah setelah deployment untuk membedakannya dari versi staging.

## 🛠️ Cara Menjalankan Proyek (Pengembangan Lokal)

1.  **Kloning Repositori**

    ```bash
    git clone [https://github.com/Ujeeg/pacmusic.git](https://github.com/Ujeeg/pacmusic.git)
    cd pacmusic
    ```

2.  **Persiapkan Variabel Lingkungan**

    ```bash
    cp .env.example .env
    ```

    * Sesuaikan isi file `.env` dengan konfigurasi lokal Anda.

3.  **Bangun dan Jalankan Aplikasi dengan Docker Compose**

    ```bash
    docker-compose up --build
    ```

4.  **Akses Aplikasi**

    Akses aplikasi di [http://localhost:8000](http://localhost:8000).

## 🧪 Pengujian

Jalankan pengujian unit:

```bash
bash test/run_tests.sh


☁️ Deployment ke AWS EC2 (Penjelasan)

    Aplikasi di-deploy ke instance AWS EC2.
    Dua instance EC2 digunakan: satu untuk staging, satu untuk production.
    GitHub Actions terhubung ke instance EC2 menggunakan kredensial AWS yang disimpan di Git Secrets.
    Docker memastikan aplikasi di-deploy dengan konsisten di kedua lingkungan.

📝 Catatan Tambahan
    Aplikasi web musik dalam proyek ini disediakan oleh bootcamp dan berfungsi sebagai contoh untuk demonstrasi CI/CD.
    Fokus utama proyek adalah pada pengaturan dan otomatisasi alur kerja CI/CD untuk pengelolaan lingkungan AWS EC2, bukan pada pengembangan fitur aplikasi musik.
