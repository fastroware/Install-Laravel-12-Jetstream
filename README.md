# Cara Install Laravel 12 dan Jetstream

1. install laravel terbarunya dulu (sekarang versi 12)
```
composer create-project laravel/laravel example-app
```
2. kemudian masuk ke folder projectnya
3. lalu jalankan kode dibawah ini untuk menginstall jetstreamnya:
```
composer require laravel/jetstream
```
4. kemudian setelah selesai, jalankan kode dibawah ini:
```
php artisan jetstream:install livewire --api --dark --verification --teams
```
## 🔧 Apa yang Terjadi Saat Perintah Dijalankan?
- Jetstream & Livewire terinstal di dalam Laravel.
- File dan view Jetstream (Blade) di-generate di folder resources/views.
- Routing autentikasi dibuat, seperti /login, /register, /dashboard, dll.
- Konfigurasi API token (Sanctum) diaktifkan, bisa digunakan untuk otentikasi API.
- Dukungan tim diaktifkan, user bisa membuat dan mengelola tim.
- Email verification diaktifkan, user wajib verifikasi email sebelum mengakses fitur tertentu.
- Dukungan dark mode diaktifkan, bisa diubah di UI.

## ⚡ Kalau Tidak Menggunakan Beberapa Opsi?
- Tanpa --api → Laravel tidak akan menginstal Sanctum untuk API authentication.
- Tanpa --dark → Tidak ada dark mode, hanya tema default.
- Tanpa --verification → User bisa langsung login tanpa perlu verifikasi email.
- Tanpa --teams → Fitur tim tidak tersedia, hanya user individual.
- Jadi, perintah ini sangat cocok buat aplikasi berbasis tim dengan API dan dark mode. 🚀
