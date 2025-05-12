
# 🎵 PacMusic

PacMusic adalah proyek pembelajaran sederhana yang bertujuan untuk memahami dan menerapkan proses Continuous Integration (CI) dan Continuous Deployment (CD) dalam pengembangan aplikasi web menggunakan GitHub Actions dan Docker.

## ✨ Fitur Utama

- CI/CD pipeline otomatis menggunakan **GitHub Actions**
- Dockerized deployment menggunakan **Docker Compose**
- Struktur proyek yang modular dan mudah dikembangkan
- Folder `test/` terdedikasi untuk unit testing
- Variabel lingkungan dikelola menggunakan file `.env`

## 🛠 Teknologi yang Digunakan

- Python
- JavaScript
- HTML & CSS
- Docker
- GitHub Actions
- Bash (untuk script testing & deployment)

## 🚀 Cara Menjalankan Proyek

Berikut adalah langkah-langkah untuk menjalankan aplikasi ini secara lokal:

```bash
# Clone repositori
git clone https://github.com/Ujeeg/pacmusic.git
cd pacmusic

# Salin file .env.example menjadi .env (jika tersedia)
cp .env.example .env

# Jalankan aplikasi menggunakan Docker Compose
docker-compose up --build
```

## 🧾 Struktur Direktori

```
pacmusic/
│
├── app/                  # Kode sumber utama aplikasi
├── test/                 # Unit testing dan integrasi
├── .github/workflows/   # File konfigurasi GitHub Actions
├── docker-compose.yml   # Konfigurasi Docker Compose
├── .env.example         # Contoh konfigurasi environment
└── README.md            # Dokumentasi proyek
```

## 🧪 Pengujian

Pengujian dilakukan dengan skrip yang terdapat di dalam folder `test/`. Jalankan pengujian dengan:

```bash
bash test/test_app.sh
```

> Pastikan semua dependensi dan environment sudah dikonfigurasi dengan benar sebelum menjalankan pengujian.

## 📌 Catatan

- Proyek ini dibuat untuk keperluan belajar CI/CD dan Docker, bukan untuk produksi.
- Pull Request dan masukan sangat diterima!

## 🤝 Kontribusi

Ingin berkontribusi? Silakan fork proyek ini dan buat pull request. Kamu juga bisa membuka issue jika menemukan bug atau punya ide pengembangan fitur baru.

## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).
