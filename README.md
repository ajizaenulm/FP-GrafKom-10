# Perencanaan Proyek Katalog Batik Tin Gundih 3D

## 1. Latar Belakang

Kampung Batik Tin Gundih memiliki produk batik yang dapat diperkenalkan melalui media digital. Calon pembeli perlu memperoleh informasi mengenai motif, bahan, ukuran, cerita produk, dan cara menghubungi pengrajin.

Proyek ini mengusulkan katalog berbasis web dengan visualisasi kain tiga dimensi. Pengunjung dapat memilih batik, memutar tampilannya secara horizontal maupun vertikal, memperbesar detail, membaca informasi produk, dan menghubungi UMKM. Kebutuhannya perlu diperiksa melalui wawancara dengan mitra. Visualisasi 3D akan dilengkapi foto produk asli.

## 2. Tujuan dan Manfaat

### Tujuan

- Menghasilkan katalog batik 3D yang dapat diakses melalui tautan publik.
- Menerapkan unsur grafika komputer sesuai ketentuan tugas.
- Menyediakan informasi produk yang telah diperiksa bersama mitra.
- Membantu pengunjung mengeksplorasi produk dan menghubungi pengrajin.
- Mendokumentasikan proses pengembangan, kontribusi anggota, dan hasil pengujian.

### Manfaat

**Bagi UMKM:**
- Memiliki media tambahan untuk memperkenalkan produk.
- Dapat menunjukkan pilihan batik secara interaktif.
- Memiliki katalog yang dapat dibagikan kepada calon pembeli.

**Bagi pengunjung:**
- Dapat melihat produk dari berbagai arah.
- Dapat membaca detail produk dan cerita motif.
- Dapat menghubungi mitra dengan menyebut produk yang diminati.

## 3. Konsep dan Batas Lingkup

### Konsep Utama

Aplikasi menampilkan satu model lembar kain dengan lipatan ringan. Pengguna memilih produk untuk mengganti tekstur motif dan informasi yang ditampilkan. Bentuk tiga dimensi harus mudah dilihat dan komposisi motif tetap mudah diamati.

### Cakupan Proyek

- Produk atau motif yang disetujui mitra
- Model kain 3D
- Pergantian tekstur sesuai produk
- Rotasi horizontal dan vertikal penuh
- Zoom dan reset tampilan
- Pencahayaan serta material kain
- Foto produk asli
- Informasi produk dan cerita motif
- Tombol kontak UMKM
- Tampilan responsif
- Alternatif foto ketika penampil 3D gagal

### Pengembangan Lanjutan

Dilakukan apabila fitur inti dan seluruh fitur telah selesai diimplementasikan:

- Dua bentuk tampilan kain: dibentangkan dan berlipat
- Titik informasi pada bagian motif
- Perbandingan dua produk
- Dashboard pengelolaan katalog
- Visualisasi pada pakaian

## 4. Alur Pengguna

1. Pengunjung membuka halaman awal
2. Pengunjung membaca pengenalan singkat mitra
3. Pengunjung memilih produk dari katalog
4. Aplikasi menampilkan model kain dan informasi produk
5. Pengunjung memutar kain dan memperbesar detail
6. Pengunjung membandingkan visualisasi dengan foto asli
7. Pengunjung membaca bahan, ukuran, cerita motif, dan ketersediaan
8. Pengunjung menekan tombol “Tanyakan Produk”
9. Aplikasi membuka kontak mitra untuk menanyakan kode atau nama produk yang diminati

## 5. Rancangan Halaman

| Halaman | Isi |
|---|---|
| Beranda | Pengenalan mitra, foto utama, dan tombol menuju katalog |
| Katalog | Card produk dengan foto, nama, dan tombol detail |
| Detail produk | Tampilan 3D, kontrol, foto asli, informasi, dan kontak |
| Tentang mitra | Profil singkat, lokasi, dokumentasi, dan kontak |

## 6. Stack Teknologi

| Kebutuhan | Teknologi | Fungsi |
|---|---|---|
| Struktur halaman | HTML | Menyusun konten dan elemen interface |
| Tampilan | CSS | Mengatur tata letak interface |
| Logika aplikasi | JavaScript | Mengelola katalog dan interaksi |
| Implementasi 3D | Three.js | Mengelola scene, kamera, model, material, dan cahaya |
| Pemodelan | Blender | Membuat kain dan koordinat UV |
| Format model | GLB | Menyimpan model untuk dimuat pada aplikasi |
| Data katalog | JSON | Menyimpan informasi produk |
| Kolaborasi | Git dan GitHub | Menyimpan kode dan riwayat kontribusi |

## 7. Rancangan Model dan Interaksi

### Model Kain

- Berbentuk lembar kain dengan lipatan
- Memiliki koordinat UV yang sesuai
- Menggunakan proporsi berdasarkan data ukuran produk
- Menampilkan sisi belakang berdasarkan dokumentasi yang tersedia

### Transformasi dan Kamera

- Rotasi objek pada sumbu X dan Y
- Perubahan skala objek
- View kamera dapat mengitari objek
- Pengaturan jarak kamera
- Tombol reset objek dan kamera

### Material dan Pencahayaan

- Material utama menggunakan MeshStandardMaterial daru Three.js
- Tekstur warna berasal dari foto motif produk
- Cahaya utama diletakkan dari arah atas-samping
- Pengaturan warna disesuaikan dengan membandingkan foto asli

## 8. Arsitektur Aplikasi

Alur data:

**Pengunjung - Interface katalog - Pemilihan produk - Data JSON - Penampil Three.js - Model dan tekstur**

Struktur kode akan dipisahkan menjadi beberapa bagian:

- Data katalog
- Interface
- Scene dan kamera
- Pemuatan model dan tekstur
- Kontrol dan transformasi
- Material dan pencahayaan
- Penanganan kegagalan pemuatan
