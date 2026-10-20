# Panduan Struktur & Pemeliharaan Portofolio

Dokumen ini menjelaskan fungsi file dan folder agar repository mudah dibaca dan aman diperbarui.

## 1. Halaman website

| File | Fungsi | Ketergantungan utama |
| --- | --- | --- |
| `index.html` | Halaman utama dan pintu masuk recruiter/client | `styles.css`, `script.js`, `assets/` |
| `recruiters.html` | Profil karier dan proyek untuk recruiter | `styles.css`, `assets/` |
| `clients.html` | Layanan dan proyek untuk calon klien | `styles.css`, `assets/` |
| `jenius-promosi.html` | Studi kasus website promosi | `styles.css`, `case-study.css`, `script.js`, `assets/` |
| `jenius-pengelola.html` | Studi kasus sistem pengelola | `styles.css`, `case-study.css`, `script.js`, `assets/` |
| `gima-analytics.html` | Studi kasus People Analytics | `styles.css`, `case-study.css`, `script.js`, `assets/` |

## 2. Tampilan dan interaksi

- **`styles.css`**: tipografi, warna, layout beranda, halaman audiens, responsivitas, dan lightbox.
- **`case-study.css`**: layout hero, fitur, galeri, dan bagian studi kasus.
- **`script.js`**: navigasi mobile, tahun footer, dan galeri interaktif.

## 3. Folder aset

Folder **`assets/`** menyimpan screenshot proyek berformat WebP. Nama file menggambarkan produk dan halaman, contohnya `jenius-promosi-beranda.webp`, `jenius-dashboard-pengelola.webp`, dan `gima-dashboard.webp`.

Jika ingin membuat subfolder `assets/jenius/` atau `assets/gima/`, semua referensi `src` dan `href` di HTML harus diperbarui bersama-sama. Jangan memindahkan gambar tanpa memperbaiki tautannya.

## 4. File teknis

- **`README.md`**: ringkasan portofolio dan panduan navigasi repository.
- **`docs/`**: dokumentasi yang tidak ditampilkan sebagai halaman portofolio.
- **`googleb9d25bc47661b5f0.html`**: file verifikasi Google Search Console yang harus tetap tersedia di root website.

## 5. Aturan pembaruan

1. Buat branch fitur untuk perubahan besar.
2. Gunakan nama file huruf kecil dan tanda hubung, misalnya `nama-halaman.html`.
3. Pastikan semua tautan internal dan gambar tetap dapat dibuka.
4. Uji tampilan desktop dan mobile, termasuk navigasi, lightbox, dan tombol WhatsApp.
5. Tinjau perubahan melalui Pull Request sebelum merge ke `main`.
6. Jangan memasukkan kata sandi, token, atau data pribadi klien ke repository.

## 6. Pengembangan berikutnya

Jika proyek bertambah besar, struktur dapat dimigrasikan menjadi `pages/`, `css/`, `js/`, dan `assets/`. Migrasi ini perlu dilakukan sebagai pekerjaan terpisah karena mengubah URL dan jalur file, sehingga membutuhkan pengujian dan kemungkinan redirect.
