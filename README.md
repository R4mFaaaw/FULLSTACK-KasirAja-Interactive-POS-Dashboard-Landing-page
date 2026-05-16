🛒 KasirAja: Interactive POS Dashboard & Landing Page

Aplikasi Kasir (Point of Sale) berbasis web yang interaktif, responsif, dan ringan. Proyek ini mengintegrasikan fungsi halaman katalog produk (*Landing Page*) dengan sistem manajemen keranjang belanja kasir (*Dashboard*) dalam satu antarmuka yang dinamis menggunakan manipulasi DOM JavaScript murni (Vanilla JS).

---

## 🎯 Fitur Utama

1. **Katalog Produk Dinamis**: Menampilkan daftar produk (makanan, minuman, cemilan) secara otomatis dari data *state* JavaScript.
2. **Pencarian Real-Time**: Fitur pencarian produk yang responsif secara langsung saat pengguna mengetik kata kunci (tanpa *reload* halaman).
3. **Manajemen Keranjang Belanja**:
   - Menambahkan produk ke keranjang secara instan.
   - Mengubah kuantitas produk (tambah/kurang) langsung dari dalam keranjang.
   - Menghapus item dari keranjang dengan tombol *trash*.
4. **Kalkulasi Otomatis (Live Calculation)**: Menghitung Subtotal, Pajak Pertambahan Nilai (PPN 11%), dan Total Akhir secara *real-time* menggunakan method `reduce()`.
5. **UI/UX Responsif & Modern**: Menggunakan Tailwind CSS versi terbaru untuk memastikan tampilan optimal di perangkat *mobile* (HP) hingga *desktop* (PC).
6. **Alur Transaksi Interaktif**: Tombol checkout yang adaptif (aktif hanya jika keranjang terisi) lengkap dengan konfirmasi sukses.

---

## 🛠️ Tech Stack yang Digunakan

* **HTML5**: Struktur semantik (`<nav>`, `<main>`, `<button>`,dll) untuk aksesibilitas dan SEO yang lebih baik.
* **Tailwind CSS v4 (via CDN)**: Framework CSS utilitas pertama untuk mempermudah desain antarmuka yang bersih, modern, dan responsif tanpa menulis file CSS terpisah.
* **FontAwesome v6**: Menyediakan ikon grafis yang representatif untuk memperkaya pengalaman visual pengguna.
* **Modern JavaScript (ES6+)**:
  - *Arrow Functions* (`=>`)
  - *Array Methods* (`.find()`, `.filter()`, `.reduce()`, `.forEach()`)
  - *Template Literals* (Backticks `` ` ``)
  - *Spread Operator* (`...`)
  - *DOM Manipulation API* (`document.createElement`, `appendChild`, `innerHTML`)

---

## 🏗️ Arsitektur Kode & Alur Data

Aplikasi ini dirancang dengan prinsip **Single Source of Truth** (Satu Sumber Data Utama), di mana UI/tampilan akan selalu menyesuaikan dengan kondisi data (*state*) saat itu.

### 1. Representasi Data (State)
Data produk disimpan dalam sebuah *Array of Objects* yang bertindak sebagai database lokal:
