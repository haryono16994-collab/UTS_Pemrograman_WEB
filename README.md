# Toko Buku UT — Proyek UTS Pemrograman Web 1
Nama: Haryono
NIM : 312510292

#Toko Buku UT
Proyek Ujian Tengah Semester (UTS) — Pemrograman Web 1
1. Deskripsi Proyek
Toko Buku UT adalah aplikasi website front-end sederhana untuk simulasi pemesanan buku secara online. Website ini dibuat sebagai pemenuhan tugas UTS Pemrograman Web 1 dengan menerapkan tiga teknologi utama, yaitu HTML, CSS, dan JavaScript.

Aplikasi menyediakan beberapa fitur, mulai dari login pengguna, dashboard, katalog dan pengelolaan stok buku, checkout, pelacakan pengiriman, laporan pemesanan, hingga riwayat transaksi.

Seluruh data pada proyek ini merupakan data dummy/simulasi. Data akun tambahan, perubahan stok, dan transaksi disimpan pada localStorage browser sehingga proyek dapat berjalan tanpa database atau server backend.
2. Tujuan Pembuatan
Tujuan pembuatan aplikasi ini adalah:
- Menerapkan struktur HTML yang semantik dan terorganisasi.
- Mengatur tampilan website menggunakan CSS eksternal.
- Menggunakan JavaScript untuk manipulasi DOM dan pengelolaan data.
- Membuat validasi form serta umpan balik kepada pengguna.
- Membuat interaksi ant halaman melalui navigasi website.
- Memahami alur sederhana pemesanan buku online dari pemilihan buku sampai pelacakan pesanan.
3. Teknologi yang Digunakan
Teknologi	Kegunaan
HTML5	Membuat struktur dan elemen setiap halaman website.
CSS3	Mengatur warna, tipografi, layout, kartu, form, modal, dan tampilan responsif.
JavaScript	Mengelola data, validasi input, event, perhitungan, dan manipulasi DOM.
Array dan Object	Menyimpan data dummy katalog buku, akun, dan tracking.
localStorage	Menyimpan data simulasi pada browser, seperti akun terdaftar, stok tambahan, dan transaksi.
Live Server (opsional)	Menjalankan website melalui server lokal saat proses pengembangan.


Tidak ada database maupun API backend yang digunakan.
4. Struktur Folder Proyek
tugas-uts-web1/
│
├── index.html             # Halaman awal / login
├── login.html             # Halaman login alternatif
├── dashboard.html         # Dashboard dan menu utama
├── stok.html              # Katalog dan pengelolaan stok buku
├── checkout.html          # Form pemesanan dan pembayaran simulasi
├── tracking.html          # Pencarian status pengiriman berdasarkan nomor DO
├── laporan.html           # Ringkasan laporan pemesanan
├── riwayat.html           # Riwayat transaksi pengguna
│
├── css/
│   └── style.css          # Seluruh aturan tampilan website
│
├── js/
│   ├── data.js            # Data dummy katalog, pengguna, dan tracking
│   └── script.js          # Logika aplikasi dan manipulasi DOM
│
├── img/
│   ├── mikrobiologi.jpg
│   ├── manajemen_keuangan.jpg
│   ├── paud_perkembangan.jpg
│   ├── kepemimpinan.jpg
│   └── pengantar_komunikasi.jpg
│
└── README.md              # Dokumentasi proyek
5. Penjelasan Halaman dan Fitur
A. Login (index.html / login.html)
Halaman login digunakan sebagai pintu masuk aplikasi. Pengguna memasukkan email dan password, kemudian JavaScript mencocokkan data dengan daftar pengguna yang tersedia.

Fitur:
- Input email dan password.
- Validasi data login.
- Pesan kesalahan apabila email atau password tidak sesuai.
- Popup/modal Daftar Akun untuk membuat akun demo baru.
- Popup/modal Lupa Password untuk mengatur ulang password akun demo.
- Pengguna yang berhasil login diarahkan ke halaman dashboard.
B. Dashboard (dashboard.html)
Dashboard merupakan halaman utama setelah pengguna berhasil login.

Fitur:
- Navigasi menuju stok buku, checkout, tracking, laporan, dan riwayat.
- Menampilkan informasi pengguna yang sedang login.
- Sapaan berdasarkan waktu lokal perangkat, seperti pagi, siang, atau malam.
- Ringkasan jumlah koleksi buku dan total stok.
C. Katalog dan Stok Buku (stok.html)
Halaman ini menampilkan daftar buku yang bersumber dari variabel dataKatalogBuku pada js/data.js.

Fitur:
- Menampilkan kode, judul, kategori/jenis, edisi, harga, stok, dan gambar buku.
- Pencarian buku berdasarkan informasi katalog.
- Form untuk menambahkan data buku baru.
- JavaScript membuat atau memperbarui elemen halaman menggunakan manipulasi DOM.
- Data buku tambahan disimpan pada localStorage agar tetap tersedia ketika halaman dimuat ulang pada browser yang sama.
D. Checkout (checkout.html)
Halaman checkout digunakan untuk membuat simulasi pesanan buku.

Fitur:
- Memilih buku dari katalog.
- Mengisi jumlah buku.
- Mengisi informasi pemesan/penerima dan alamat pengiriman.
- Memilih metode pembayaran simulasi.
- Menghitung total harga berdasarkan harga buku dan jumlah pesanan.
- Validasi input sebelum pesanan diproses.
- Membuat nomor Delivery Order (DO) untuk digunakan pada halaman tracking.
- Menyimpan data pesanan dan transaksi ke localStorage.
E. Tracking Pengiriman (tracking.html)
Halaman tracking digunakan untuk mencari pesanan menggunakan nomor Delivery Order (DO).

Informasi yang dapat ditampilkan:
- Nama pemesan.
- Nomor DO.
- Informasi buku dan jumlah pesanan.
- Detail ekspedisi dan tanggal pengiriman sesuai data simulasi.
- Jenis paket dan total pembayaran.
- Status perjalanan paket melalui tampilan timeline/progres.
Status pengiriman merupakan simulasi, bukan informasi real-time dari perusahaan ekspedisi.
F. Laporan Pemesanan (laporan.html)
Halaman laporan menampilkan ringkasan transaksi yang tersimpan pada browser, seperti jumlah pesanan dan nilai transaksi. Data laporan berasal dari transaksi simulasi yang dibuat melalui halaman checkout.
G. History Transaksi (riwayat.html)
Halaman ini menampilkan daftar transaksi yang pernah dibuat pada browser yang sama. Pengguna dapat melihat informasi pesanan dan menggunakan tombol lacak untuk membuka halaman tracking berdasarkan nomor DO.
6. Penerapan JavaScript
JavaScript pada proyek ini digunakan untuk membuat website lebih interaktif. Penerapannya meliputi:
1. Pengambilan elemen DOM
   Mengakses elemen HTML menggunakan metode seperti document.getElementById() dan document.querySelector().
2. Event handling
   Menangani aksi pengguna seperti klik tombol, pengiriman form, perubahan pilihan buku, dan pencarian.
3. Manipulasi DOM
   Menampilkan katalog, menambahkan baris stok, memperbarui ringkasan, serta menampilkan hasil tracking secara dinamis.
4. Validasi form
   Memeriksa kelengkapan dan kesesuaian input login, pendaftaran akun, reset password, stok, dan checkout.
5. Pengolahan data
   Menggunakan array dan object untuk membaca, mencari, menyaring, serta mengolah data katalog dan transaksi.
6. Perhitungan otomatis
   Menghitung total checkout berdasarkan harga buku dan jumlah yang dipesan.
7. Penyimpanan lokal
   Menggunakan localStorage untuk menyimpan sesi login demo, akun tambahan, stok tambahan, dan transaksi.
7. Cara Menjalankan Website
1. Unduh dan ekstrak file proyek.
2. Buka folder tugas-uts-web1 menggunakan Visual Studio Code.
3. Pastikan struktur folder tidak berubah agar tautan CSS, JavaScript, dan gambar tetap sesuai.
4. Jalankan file index.html menggunakan ekstensi Live Server atau buka langsung melalui browser.
5. Login menggunakan salah satu akun demo di bawah.
6. Coba alur aplikasi: dashboard → stok buku → checkout → tracking → laporan/riwayat.
8. Akun Demo
Peran	Email	Password
User	rina@gmail.com	rina123
User	agus@gmail.com	agus123
Admin	siti@gmail.com	siti123


Akun di atas hanya untuk demonstrasi tugas. Sistem role belum menjadi sistem hak akses backend yang aman.
9. Contoh Alur Pengujian
1. Buka halaman login dan coba masukkan password yang salah untuk melihat validasi.
2. Buka popup daftar akun dan buat akun demo baru.
3. Login menggunakan akun yang tersedia.
4. Pada dashboard, buka halaman stok buku.
5. Cari buku tertentu dan tambahkan satu data stok baru.
6. Buka checkout, pilih buku, masukkan jumlah, dan lengkapi data pemesan.
7. Proses pesanan dan catat nomor DO yang dihasilkan.
8. Buka tracking, masukkan nomor DO tersebut, lalu tekan tombol cari/lacak.
9. Buka laporan dan riwayat untuk melihat transaksi yang sudah dibuat.
10. Batasan Aplikasi
Proyek ini merupakan aplikasi front-end untuk keperluan pembelajaran, sehingga memiliki batasan berikut:
- Data disimpan di localStorage, bukan database server.
- Data hanya tersedia pada browser dan perangkat tempat data dibuat.
- Menghapus data situs/browser dapat menghapus akun tambahan, stok tambahan, dan transaksi demo.
- Login dan pengelolaan password belum menggunakan autentikasi server atau enkripsi password yang layak untuk produksi.
- Fitur lupa password hanya mengubah password pada simulasi lokal; tidak mengirim email verifikasi.
- Pembayaran tidak terhubung dengan bank atau payment gateway.
- Tracking tidak terhubung dengan API ekspedisi dan tidak menunjukkan posisi paket sungguhan.
- Aplikasi belum ditujukan untuk penggunaan transaksi komersial.
11. Kesimpulan
Melalui proyek Toko Buku UT, konsep dasar pengembangan website front-end diterapkan dalam bentuk aplikasi pemesanan buku online. HTML digunakan untuk membangun struktur halaman, CSS untuk mengatur desain dan responsivitas, sedangkan JavaScript digunakan untuk validasi form, manipulasi DOM, pengolahan data, perhitungan checkout, serta penyimpanan transaksi secara lokal.

Proyek ini menjadi latihan untuk memahami hubungan antara struktur HTML, tampilan CSS, dan interaksi JavaScript dalam membangun sebuah aplikasi web sederhana.
Mata Kuliah: Pemrograman Web 1
Jenis Tugas: Ujian Tengah Semester (UTS)
Nama Proyek: Toko Buku UT — Aplikasi Pemesanan Buku Online
