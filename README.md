# DAWET — Belajar Web Development dari Nol

> **Learn. Build. Understand.**

Repo ini berisi materi, modul, dan kode contoh program belajar web development **DAWET** — Fase 1: *Web Foundation*. Materi disusun bertahap, mulai dari HTML, CSS, layout, responsive design, Git & GitHub, sampai dasar JavaScript.

Setiap folder adalah satu pertemuan/modul yang berdiri sendiri, lengkap dengan modul bacaan (PDF/PPTX), kode contoh, praktik, dan checkpoint.

---

## Daftar Isi

- [Peta Kurikulum](#peta-kurikulum)
- [Alur Belajar](#alur-belajar)
- [Struktur Repo](#struktur-repo)
- [Cara Menggunakan Repo](#cara-menggunakan-repo)
- [Konvensi Penamaan](#konvensi-penamaan)
- [Catatan Fase](#catatan-fase)

---

## Peta Kurikulum

| # | Folder | Topik | Materi | Kode contoh |
|---|--------|-------|--------|-------------|
| 01 | [`01-pengenalan-html`](01-pengenalan-html/README.md) | Pengenalan HTML & halaman pertama | — | `index.html` |
| 02 | [`02-html-dasar`](02-html-dasar/README.md) | HTML Dasar: tag, element, attribute, heading, list, link, image | PDF, TeX, PPTX | `index.html`, `index2.html`, `latihan/` |
| 03 | [`03-html-lanjutan`](03-html-lanjutan/README.md) | HTML Lanjutan: hyperlink, relative path, semantic HTML, multi-page | PDF, TeX, PPTX | `index.html`, `info_pribadi.html`, `contact.html` |
| 04 | [`04-css-dasar`](04-css-dasar/README.md) | CSS Dasar: selector, warna, tipografi, box model, styling navigasi | PDF, TeX, PPTX | `codingan-na/` |
| 05 | [`05-css-layout-flexbox-grid`](05-css-layout-flexbox-grid/README.md) | CSS Layout: container & item, Flexbox, CSS Grid | PDF, TeX | — |
| 06 | [`06-responsive-web-design`](06-responsive-web-design/README.md) | Responsive Web Design: viewport, satuan relatif, media queries | PDF | — |
| 07 | [`07-git-github-dokumentasi`](07-git-github-dokumentasi/README.md) | Git & GitHub serta dokumentasi proyek dengan README.md | PDF | — |
| 08 | [`08-javascript-dasar`](08-javascript-dasar/README.md) | JavaScript Dasar: variabel, operator, percabangan, perulangan, fungsi, array, object | PDF, TeX | — |

---

## Alur Belajar

```
HTML Dasar ──► HTML Lanjutan ──► CSS Dasar ──► CSS Layout
   (02)            (03)             (04)           (05)
                                                    │
                                                    ▼
JavaScript ◄── Git & GitHub ◄── Responsive Web Design
   (08)            (07)                (06)
```

Urutan yang disarankan:

1. **Modul 01–03** — bangun fondasi struktur halaman: satu halaman, lalu website multi-page.
2. **Modul 04** — pelajari cara memberi tampilan pada struktur yang sudah ada.
3. **Modul 05–06** — susun layout dengan Flexbox/Grid, lalu buat tampilan menyesuaikan ukuran layar.
4. **Modul 07** — unggah dan dokumentasikan proyek di GitHub.
5. **Modul 08** — tambahkan interaksi dan logika dengan JavaScript.

Modul 02–07 merupakan bekal untuk menyelesaikan **Pra-Assignment 1: Web Foundation**. Modul 08 menjadi jembatan menuju tahap JavaScript.

---

## Struktur Repo

```
dawet-belajar-genzme/
├── README.md                        ← kamu di sini (peta kurikulum)
│
├── 01-pengenalan-html/
│   └── README.md + index.html
├── 02-html-dasar/
│   ├── README.md
│   ├── DAWET_Meeting_02_HTML_Dasar_Modul.pdf / .tex
│   ├── DAWET_Meeting_02_HTML_Dasar_Modern.pptx
│   ├── index.html, index2.html
│   ├── img1.jpg, referensi.jpg
│   └── latihan/                     ← latihan multi-page + Bootstrap
├── 03-html-lanjutan/
│   ├── README.md
│   ├── DAWET_Meeting_03_HTML_Lanjutan_Modul.pdf / .tex
│   ├── DAWET_Meeting_03_HTML_Lanjutan_Modern.pptx
│   └── index.html, info_pribadi.html, contact.html
├── 04-css-dasar/
│   ├── README.md
│   ├── DAWET_Week_04_CSS_Dasar_Modul_Rinci.pdf / .tex
│   ├── DAWET_Week_04_CSS_Dasar_Modern.pptx
│   └── codingan-na/                 ← contoh HTML + CSS
├── 05-css-layout-flexbox-grid/
│   ├── README.md
│   └── DAWET_Minggu_5_Pra_Assignment_1_CSS_Layout.pdf / .tex
├── 06-responsive-web-design/
│   ├── README.md
│   └── DAWET_Minggu_6_Pra_Assignment_1_Responsive_Web_Design.pdf
├── 07-git-github-dokumentasi/
│   ├── README.md
│   └── Pertemuan 7 - Github & Dokumentasi.pdf
└── 08-javascript-dasar/
    ├── README.md
    └── Pertemuan 8 - JavaScript.pdf / .tex
```

---

## Cara Menggunakan Repo

**Membaca materi**

Buka file PDF di folder modul. File `.tex` disediakan bagi yang ingin mempelajari atau mengubah sumber modul (butuh LaTeX untuk kompilasi). File `.pptx` adalah versi presentasi.

**Menjalankan kode contoh**

Tidak perlu server atau instalasi apa pun:

1. Buka folder modul.
2. Klik dua kali `index.html`, atau klik kanan → *Open with* → browser.
3. Untuk modul 04, buka `04-css-dasar/codingan-na/index.html` (CSS eksternal sudah terhubung).

Alternatif: gunakan ekstensi **Live Server** di VS Code agar halaman otomatis *reload* setiap kali file disimpan.

**Mengerjakan latihan**

Setiap README modul memuat bagian *Praktik & Tugas* dan *Checkpoint Pemahaman*. Kerjakan di folder terpisah agar kode contoh tetap utuh.

---

## Konvensi Penamaan

- Folder modul: `NN-topik-kebab-case` — angka dua digit untuk urutan, huruf kecil, tanpa spasi.
- README modul: selalu `README.md` di dalam folder modul (GitHub merender otomatis).
- Nama file modul mengikuti pola `DAWET_<Pertemuan>_<Topik>_Modul.<ext>`.
- Setiap modul menautkan modul sebelum dan sesudahnya pada bagian **Navigasi**.

---

## Catatan Fase

| Tahap | Cakupan |
|-------|---------|
| **Fase 1 — Web Foundation** | Modul 01–07: HTML, CSS, CSS Layout, Responsive Design, Git & GitHub |
| **Lanjutan** | Modul 08: JavaScript Dasar sebagai fondasi interaksi |

Modul 05 dan 06 sama-sama bagian dari rangkaian **Pra-Assignment 1** (Fase 1). Modul 07 menutup fase dengan pengumpulan proyek ke GitHub beserta dokumentasinya.

---

*Dokumen ini adalah peta kurikulum. Untuk penjelasan lengkap setiap topik, buka `README.md` di folder modul yang bersangkutan.*
