# 🎵 PacMusic - CI/CD Web Application

PacMusic adalah aplikasi web musik yang menerapkan prinsip Continuous Integration (CI) dan Continuous Deployment (CD) menggunakan GitHub Actions, Docker, dan Git Secrets. Aplikasi ini akan dideploy ke AWS EC2 dengan dua lingkungan: staging dan production.

## 🚀 Tujuan Proyek
- Automatisasi pengujian dan deployment aplikasi.
- Menggunakan GitHub Actions, Docker, dan Git Secrets.
- Menyediakan dua lingkungan: Staging dan Production.

## 🔧 Teknologi yang Digunakan
- **CI/CD**: GitHub Actions
- **Containerization**: Docker
- **Cloud**: AWS EC2
- **Keamanan**: Git Secrets

## ⚙️ Alur Kerja CI/CD

### Staging Environment:
- Menggunakan GitHub Actions untuk build dan pengujian aplikasi di staging.
  
### Production Deployment:
- Setelah pengujian di staging, deployment otomatis ke production dengan versi baru.

## 🛠️ Cara Menjalankan Proyek

1. **Kloning Repositori**
    ```bash
    git clone https://github.com/Ujeeg/pacmusic.git
    cd pacmusic
    ```

2. **Persiapkan Variabel Lingkungan**
    ```bash
    cp .env.example .env
    ```

3. **Bangun dan Jalankan Aplikasi**
    ```bash
    docker-compose up --build
    ```

4. **Akses Aplikasi**
    Akses aplikasi di [http://localhost:8000](http://localhost:8000).

## 🧪 Pengujian

Jalankan pengujian unit:
```bash
bash test/run_tests.sh



📂 Struktur Proyek
    ```
pacmusic/
├── app/
├── test/
├── .github/workflows/
├── docker-compose.yaml
├── .env.example
└── README.md
    ```
