# Modul 03 — HTML Lanjutan

**Fase 1 · Web Foundation · Pertemuan 3**

> Dari satu halaman menjadi website: hyperlink, navigasi, relative path, dan semantic HTML.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan fungsi hyperlink.
2. Membuat link ke website lain.
3. Membuat link antar halaman HTML.
4. Memahami relative path sederhana.
5. Membuat navigasi dengan `<nav>`.
6. Memahami dasar `<section>` dan `<article>`.
7. Membuat website sederhana multi-page.

---

## Ringkasan Materi

### 1. Hyperlink dengan `<a>`

```html
<a href="https://www.instagram.com/">Instagram</a>
<a href="https://maps.google.com/">Google Maps</a>
```

`href` menentukan tujuan link; teks di antara tag pembuka dan penutup menjadi bagian yang bisa diklik. Link eksternal memakai URL lengkap (`https://...`).

### 2. Link Antar Halaman dan Relative Path

```
portal-umkm/
├── index.html
├── tentang.html
├── produk.html
└── kontak.html
```

```html
<!-- dari index.html -->
<a href="tentang.html">Tentang</a>
```

| Path | Arti |
|------|------|
| `tentang.html` | File di folder yang sama |
| `images/logo.png` | File di subfolder `images/` |
| `../index.html` | Naik satu folder, lalu buka `index.html` |
| `/index.html` | Dari root website |

Path pada `href` bekerja dengan logika yang sama seperti `src` pada gambar.

### 3. Navigasi dengan `<nav>`

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="tentang.html">Tentang</a></li>
        <li><a href="produk.html">Produk</a></li>
        <li><a href="kontak.html">Kontak</a></li>
    </ul>
</nav>
```

Membungkus kumpulan link utama dengan `<nav>` memberi makna bahwa itu adalah navigasi situs.

### 4. Semantic HTML

Semantic HTML adalah penggunaan tag yang menjelaskan **makna** konten, bukan hanya tampilannya.

| Tag | Fungsi |
|-----|--------|
| `<header>` | Bagian pembuka halaman/section: judul, logo |
| `<nav>` | Kumpulan link navigasi |
| `<main>` | Konten utama halaman (hanya satu per halaman) |
| `<section>` | Pengelompokan konten dengan tema yang sama |
| `<article>` | Konten mandiri yang bisa berdiri sendiri (berita, kartu produk) |
| `<footer>` | Bagian penutup: copyright, kontak, link tambahan |

```html
<body>
    <header>
        <h1>Portal UMKM</h1>
        <nav>...</nav>
    </header>
    <main>
        <section>
            <h2>Produk Unggulan</h2>
            <article>
                <h3>Keripik Singkong</h3>
                <p>Renyah, cocok untuk camilan.</p>
            </article>
        </section>
    </main>
    <footer>
        <p>&copy; 2026 Portal UMKM</p>
    </footer>
</body>
```

### 5. Membangun Website Multi-page

Halaman-halaman dihubungkan dengan link relatif, memiliki struktur dasar yang konsisten, dan memakai elemen semantic secara masuk akal. Ini adalah langkah dari "satu dokumen" menjadi "satu website".

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `DAWET_Meeting_03_HTML_Lanjutan_Modul.pdf` | Modul bacaan lengkap |
| `DAWET_Meeting_03_HTML_Lanjutan_Modul.tex` | Sumber LaTeX modul |
| `DAWET_Meeting_03_HTML_Lanjutan_Modern.pptx` | Slide presentasi |
| `index.html` | Demo utama: `header`, `nav`, `main`, `footer`, semantic element, link internal & eksternal |
| `info_pribadi.html` | Halaman kedua dengan navigasi kembali ke `index.html` |
| `contact.html` | Halaman kontak |
| `img1.jpg` | Aset gambar demo |

**Catatan:** navigasi di `index.html` juga menautkan ke `../01-pengenalan-html/index.html` sebagai contoh link ke folder modul sebelumnya.

---

## Praktik & Tugas

Kembangkan halaman Modul 02 menjadi website kecil dengan minimal **Home, Tentang, dan Produk**.

**Ketentuan:**

1. Minimal tiga file HTML.
2. Struktur dasar lengkap pada setiap halaman.
3. Navigasi yang menghubungkan halaman.
4. Minimal satu link eksternal.
5. Penggunaan `header`, `nav`, `main`, `section`, dan `footer` secara masuk akal.
6. Minimal satu gambar.

**Bonus:** halaman Kontak, Google Maps, Instagram/WhatsApp, folder gambar yang rapi, dan `<article>` untuk konten mandiri.

**Tugas GitHub:** simpan dalam struktur `minggu-03/portal-umkm/`, lakukan commit & push, lalu isi README dengan struktur halaman, daftar link, semantic element yang dipakai, kendala, hal baru, dan screenshot.

---

## Checkpoint Pemahaman

1. Apa perbedaan link eksternal dan internal?
2. Apa fungsi `href`?
3. Mengapa cara kerja path `href` mirip dengan `src`?
4. Mengapa kumpulan link navigasi dibungkus dengan `<nav>`?
5. Apa fungsi `<section>`?
6. Kapan `<article>` masuk akal digunakan?
7. Apa yang dimaksud semantic HTML?

---

## Persiapan Menuju CSS

Website pada tahap ini mungkin masih terlihat polos — itu normal. HTML menyusun struktur dan makna; CSS yang akan mengatur warna, ukuran teks, jarak, border, dan layout. Jangan terlalu sibuk mempercantik HTML secara manual.

---

## Referensi

- MDN — [`<a>` Anchor Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/a)
- MDN — [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/nav)
- MDN — [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 02 — HTML Dasar](../02-html-dasar/README.md) | [Modul 04 — CSS Dasar](../04-css-dasar/README.md) |
