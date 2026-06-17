<div align="center">
  <img src="public/images/logo.png" alt="Logo Himpunan" width="150"/>
  <h1>Sistem Absensi Himpunan Berbasis QR Code</h1>
  <p>Aplikasi pencatatan presensi modern, responsif, dan komprehensif untuk organisasi dan himpunan mahasiswa, dikembangkan menggunakan Laravel 11 dan Tailwind CSS.</p>
</div>

---

## ✨ Fitur Utama

### 👑 Modul Admin
- **Manajemen Kegiatan (CRUD):** Jadwalkan acara, rapat, atau kegiatan himpunan.
- **Generate QR Code Absensi:** Buat kode QR unik per kegiatan yang dapat diperbarui (*regenerate*) secara instan.
- **Manajemen Anggota:** Kelola data anggota dan pembuatan akun login otomatis.
- **Rekapitulasi Laporan Kehadiran:** Lihat statistik kehadiran, daftar izin/sakit, dan unduh laporan dalam format **PDF** maupun **Excel (XLSX)**.
- **UI/UX Premium:** Antarmuka dengan efek *glassmorphism*, animasi mikro, dan *gradient blobs* yang elegan.

### 👤 Modul Anggota
- **Scan QR Code:** Rekam kehadiran dengan cepat menggunakan *scanner* bawaan kamera *smartphone* atau laptop.
- **Pengajuan Izin & Sakit:** Formulir pengajuan izin/sakit yang mewajibkan unggah berkas surat keterangan (PDF/JPG/PNG).
- **Dasbor Pribadi:** Antarmuka menarik untuk memantau status anggota.

---

## 🛠️ Teknologi yang Digunakan

- **Framework:** [Laravel 11](https://laravel.com/) (PHP)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) dengan tipografi *Outfit*
- **Frontend Interactivity:** [Alpine.js](https://alpinejs.dev/)
- **PDF Generator:** [barryvdh/laravel-dompdf](https://github.com/barryvdh/laravel-dompdf)
- **Excel Generator:** [Maatwebsite/Laravel-Excel](https://laravel-excel.com/)
- **QR Code & Scanner:** `simplesoftwareio/simple-qrcode` & HTML5 QR Code Scanner

---

## 🚀 Panduan Instalasi (Local Development)

Ikuti langkah-langkah di bawah ini untuk menjalankan aplikasi ini di komputer lokal Anda:

1. **Kloning Repository**
   ```bash
   git clone https://github.com/USERNAME/sistem-absensi-himpunan.git
   cd sistem-absensi-himpunan
   ```

2. **Instalasi Dependensi PHP & Node.js**
   ```bash
   composer install
   npm install
   ```

3. **Konfigurasi Environment**
   Salin *file* konfigurasi bawaan dan *generate* kunci aplikasi:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
   *Buka file `.env` dan atur koneksi database Anda (contoh: SQLite atau MySQL).*

4. **Jalankan Migrasi & Tautkan Storage (Wajib untuk file Izin/Logo)**
   ```bash
   php artisan migrate
   php artisan storage:link
   ```

5. **Kompilasi Aset Frontend (Tailwind)**
   ```bash
   npm run build
   # Atau jika sedang tahap development: npm run dev
   ```

6. **Jalankan Server Lokal**
   ```bash
   php artisan serve
   ```
   *Aplikasi kini dapat diakses di `http://127.0.0.1:8000`*

---

## 🔐 Info Login Default
Secara bawaan, anggota yang baru diregistrasikan oleh Admin akan menggunakan kredensial:
- **Email:** `(email-anggota@example.com)`
- **Password:** `himpunan123`

---

## 📝 Lisensi
Proyek ini bersifat *Open-Source* dan tersedia di bawah Lisensi MIT.
