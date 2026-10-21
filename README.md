# hackathon

Situs statis sederhana (HTML, CSS, JavaScript murni) tanpa dependensi dan tanpa build step.

## Struktur proyek

```
hackathon/
├── index.html          # Halaman utama (header, hero, tentang, fitur, kontak, footer)
├── siap-serah.html     # Prototipe hackathon: cek kelengkapan berkas pajak (satu file, berisi data contoh)
├── assets/
│   ├── css/
│   │   └── style.css   # Gaya global: variabel warna, mode gelap, layout responsif
│   └── js/
│       └── main.js     # Skrip kecil di sisi klien (mis. tahun di footer)
└── README.md           # Dokumentasi proyek
```

| Path | Fungsi |
| --- | --- |
| `index.html` | Titik masuk situs. Memuat `style.css` di `<head>` dan `main.js` di akhir `<body>`. |
| `siap-serah.html` | Prototipe "Siap Serah". Mandiri (CSS, JS, dan data contoh ada di satu file). Data contoh ada di objek `DATA` di bagian `<script>`. |
| `assets/css/style.css` | Semua styling. Warna didefinisikan sebagai variabel CSS di `:root` dan otomatis berganti saat sistem memakai mode gelap. |
| `assets/js/main.js` | Logika interaktif. Diletakkan di akhir `<body>` agar DOM sudah siap saat skrip berjalan. |
| `assets/` | Tempat semua aset statis. Tambahkan `assets/img/` untuk gambar bila diperlukan. |

## Menjalankan secara lokal

Buka `index.html` langsung di browser, atau jalankan server statis:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## Menambah halaman baru

1. Salin `index.html` menjadi misalnya `about.html`.
2. Ubah isi `<main>` dan `<title>`.
3. Tambahkan tautannya di `<nav>` pada setiap halaman.
