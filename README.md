# Consent Location Tracker

Versi ini menggunakan:
- GitHub Pages untuk hosting frontend.
- Supabase untuk database + login dashboard.
- Browser Geolocation API untuk meminta izin lokasi.
- Google Maps untuk membuka koordinat.

## Setup

1. Buat project Supabase.
2. Buka SQL Editor dan jalankan `supabase.sql`.
3. Aktifkan Email/Password di Authentication.
4. Buat akun admin di Supabase Authentication.
5. Salin `config.example.js` menjadi `config.js`.
6. Isi `SUPABASE_URL` dan `SUPABASE_ANON_KEY` dari Project Settings > API.
7. Upload semua file ke repository GitHub Pages.
8. Pastikan folder `t/` dan file `t/index.html` ikut ter-upload.

## Cara pakai

Buka `index.html`, masukkan URL tujuan dan slug.
Contoh hasil:
https://username.github.io/nama-repo/t/dikarchetype

Ketika dibuka:
- Pengunjung melihat penjelasan.
- Mereka dapat memilih lanjut tanpa lokasi, atau meminta izin lokasi.
- Jika mereka mengizinkan, koordinat dan nama perangkat yang dapat dideteksi browser dicatat.
- Setelah itu pengunjung diarahkan ke URL tujuan.

## Catatan domain

Kamu tidak dapat membuat:
https://vt.tiktok.com/ZSby1hxC4/dikarchetype

karena `vt.tiktok.com` bukan domain yang kamu kuasai.

Gunakan domain milikmu sendiri, misalnya:
https://username.github.io/tracker/t/dikarchetype

Atau hubungkan domain sendiri ke GitHub Pages.

## Persistensi

Data tersimpan di Supabase, bukan localStorage browser. Jadi data tetap ada walaupun halaman atau HP kamu ditutup, selama project/database tetap aktif dan datanya tidak dihapus.

## Privasi

Gunakan sistem ini hanya untuk pengumpulan lokasi yang jelas-jelas disetujui pengguna. Jangan menyamarkan permintaan lokasi atau mencoba melewati izin browser.
