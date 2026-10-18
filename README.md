# Our Little Story ♡ — Website Ulang Tahun

Website statis romantis untuk dipublikasikan gratis dengan GitHub Pages.

## Isi
- PIN rahasia 6 digit
- Halaman ucapan ulang tahun dengan animasi
- Timeline perjalanan hubungan
- Countdown menuju anniversary pertama: 19 Maret 2027
- Galeri Polaroid dengan animasi berputar
- Surat ulang tahun panjang
- Form harapan umur 19 tahun dan harapan untuk pasangan

## 1. Personalisasi
Buka `index.html` dan cari bagian `PERSONALISASI WEBSITE` di dekat bagian bawah file.

- `SECRET_PIN = "190327"`: ganti menjadi PIN rahasia 6 digit.
- `HER_NAME = "sayang"`: ganti dengan nama/panggilan pacar.
- `MY_NAME = "your person"`: ganti dengan namamu.
- `JOURNEY`: ganti tanggal, judul, cerita, dan nama file foto.
- `GALLERY`: ganti caption dan nama file foto.
- `LOVE_LETTER`: ubah surat agar sesuai cerita kalian.

Catatan: PIN di website statis adalah pengunci kejutan sederhana, bukan keamanan sungguhan. Siapa pun yang memahami kode sumber dapat menemukan PIN.

## 2. Memasukkan foto kalian
Letakkan foto di folder `photos/`, lalu gunakan nama file berikut (atau sesuaikan nama di kode):
- `foto1.jpg` sampai `foto3.jpg`: foto timeline
- `foto4.jpg` sampai `foto9.jpg`: foto galeri

Format JPG paling mudah. Jika fotomu PNG, ubah ekstensi di `index.html` menjadi `.png`.
Gunakan foto yang memang ingin kamu bagikan melalui website. Foto yang berada di repositori publik bisa dilihat siapa saja yang memiliki link.

## 3. Agar formulir harapan bisa kamu terima online
Secara default, ketika formulir dikirim, browser mengunduh jawaban sebagai file `.txt` di perangkat pacarmu. Website GitHub Pages tidak punya database bawaan, jadi file jawaban tidak otomatis terkirim kepadamu.

Pilihan sederhana:
1. Buat form endpoint di layanan seperti FormSubmit atau Formspree.
2. Ikuti langkah verifikasi dan konfigurasi yang ditampilkan layanan tersebut.
3. Salin endpoint pengiriman yang disediakan layanan.
4. Tempelkan ke `const FORM_ENDPOINT = "";` di `index.html`.
5. Pastikan endpoint menerima JSON dengan field `nama`, `harapan_umur_19`, `harapan_untuk_kita`, `harapan_untuk_kamu`, dan `pesan_tambahan`. Jika layanan mengharuskan format lain, handler submit di bagian akhir file perlu disesuaikan.

Jangan masukkan password, token privat, atau API secret ke kode frontend publik.

## 4. Publikasikan melalui GitHub Pages
1. Login ke https://github.com
2. Klik tombol **+** di kanan atas → **New repository**.
3. Beri nama repo, misalnya `our-little-story`. Pilih **Public** (atau cek ketersediaan Pages untuk repo private pada akunmu).
4. Klik **Create repository**.
5. Klik **Add file** → **Upload files**.
6. Unggah `index.html`, `README.md`, dan folder `photos` beserta foto kalian.
7. Klik **Commit changes**.
8. Buka **Settings** → **Pages**.
9. Pada **Build and deployment**, pilih **Deploy from a branch**.
10. Pilih branch `main`, folder `/(root)`, lalu **Save**.
11. Tunggu proses deploy selesai. Link akan muncul di halaman Pages, biasanya berbentuk `https://USERNAME.github.io/our-little-story/`.

Setiap kali mengubah file, commit perubahan ke GitHub. Tunggu beberapa saat sampai website diperbarui.

## 5. Sebelum dikirim ke pacar
- Coba PIN yang benar dan salah.
- Pastikan nama dan semua tanggal sudah sesuai.
- Uji di layar HP.
- Isi semua file foto dengan foto kalian.
- Uji formulir. Untuk mode default, pastikan file `.txt` terunduh. Untuk pengiriman online, uji endpoint layanan formulir.
