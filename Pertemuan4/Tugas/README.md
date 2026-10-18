# Laporan Tugas Praktikum Desain Web Pertemuan 4

## A. Tugas Individu: Halaman Profil (`tugas-individu-profil/`)
File: `index.html` dan `style.css` (CSS dipisah ke file eksternal lewat `<link rel="stylesheet">`).

### Penerapan konsep
- **Box model**: `* { box-sizing: border-box }` agar `width` sudah termasuk padding dan border. `.card` memakai padding 20px, border 1px, dan jarak antar card diatur dengan `gap`; `.container` memakai margin `0 auto` untuk memusatkan konten.
- **Class reusable**: `.container` (pembungkus lebar maksimum), `.section` (jarak vertikal antar bagian), `.card` (3 kartu proyek), dan `.button` (tombol).
- **Media query** `max-width: 767px` (di bawah 768px): header berubah menjadi tersusun vertikal dan 3 card berubah dari berjajar menjadi 1 kolom.

### Daftar perubahan
| Bagian | Sebelum | Sesudah |
|---|---|---|
| Header | Statis | `position: sticky; top: 0; z-index: 1000`, Flexbox `space-between` (judul kiri, menu kanan) |
| Card | Tampilan dasar | Latar `#ffffff`, `box-shadow: 0 4px 8px rgba(0,0,0,.1)`, hover `translateY(-5px)` dengan `transition` |
| Tombol | Kotak biasa | `border-radius: 25px` (pill), hover `#2e7d32` dengan teks putih |
| Footer | Polos | Latar `#366da3`, font 14px, `border-top: 2px solid #ffffff33`, padding 20px |

### Masalah dan solusi
1. **Anchor tertutup header sticky** saat menu diklik. Solusi: `scroll-padding-top: 80px` pada `html`.
2. **Lebar elemen melebihi layar** karena padding menambah lebar. Solusi: `box-sizing: border-box`.
3. **Card tidak muat di ponsel** saat berjajar. Solusi: media query yang mengubah `flex-direction` menjadi `column`.
4. **Efek hover terasa kasar**. Solusi: `transition: transform 0.3s ease`.

## B. Studi Kasus: Landing Page Arunika Studio (`studi-kasus-arunika/`)
Konten: header, hero, tiga layanan, footer.

- **CSS tidak tersebar**: seluruh gaya ada di satu `style.css`, tanpa atribut `style=""` maupun tag `<style>` di HTML.
- **3 card menjadi 1 kolom**: desktop memakai `grid-template-columns: repeat(3, 1fr)`; pada `max-width: 767px` diubah menjadi `1fr`.
- **Masalah**: card menjadi sempit dan teks sulit dibaca di ponsel. **Solusi**: satu kolom penuh, ukuran judul hero dikecilkan, padding hero dikurangi.

## Hasil PC

## Hasil Mobile