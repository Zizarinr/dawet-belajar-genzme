# Modul 02 — HTML Dasar

**Fase 1 · Web Foundation · Pertemuan 2**

> Dari struktur HTML dasar menuju fondasi Portal UMKM Kampus.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan fungsi HTML dalam website.
2. Membedakan tag, element, dan attribute.
3. Membuat struktur dasar dokumen HTML.
4. Menggunakan heading, paragraph, list, link, dan image.
5. Membuat halaman profil UMKM sederhana.

---

## Ringkasan Materi

### 1. Apa Itu HTML?

HTML adalah *markup language* yang menyusun struktur dan memberi makna pada konten halaman web. Analogi yang dipakai di modul:

| Teknologi | Peran |
|-----------|-------|
| HTML | Struktur dan ruangan rumah |
| CSS | Warna, dekorasi, dan tampilan |
| JavaScript | Interaksi dan perilaku |

### 2. Tag, Element, dan Attribute

```html
<a href="https://example.com">Kunjungi website</a>
```

- **Tag** — penanda dalam kurung sudut: `<a>` (pembuka) dan `</a>` (penutup).
- **Element** — keseluruhan tag pembuka + isi + tag penutup.
- **Attribute** — informasi tambahan pada tag, misalnya `href` yang berisi alamat tujuan.

### 3. Struktur Dasar HTML

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Halaman Saya</title>
</head>
<body>
    <h1>Hello, DAWET!</h1>
    <p>Ini halaman web pertama saya.</p>
</body>
</html>
```

| Bagian | Fungsi |
|--------|--------|
| `<!DOCTYPE html>` | Memberi tahu browser bahwa dokumen memakai HTML5 |
| `<html lang="id">` | Elemen akar; `lang` menandai bahasa dokumen |
| `<head>` | Metadata: judul, charset, referensi CSS |
| `<body>` | Konten utama yang tampil di browser |

### 4. Heading dan Paragraph

Heading tersedia dari `<h1>` sampai `<h6>`. Gunakan berdasarkan tingkat kepentingan struktur konten, bukan sekadar memperbesar teks.

```html
<h1>Warung Berkah</h1>
<h2>Menu Favorit</h2>
<p>Kami menyediakan makanan rumahan dengan harga bersahabat.</p>
```

### 5. List

```html
<!-- Unordered list: tanpa urutan -->
<ul>
    <li>Nasi Goreng</li>
    <li>Mie Ayam</li>
</ul>

<!-- Ordered list: berurutan -->
<ol>
    <li>Pilih menu</li>
    <li>Hubungi penjual</li>
    <li>Konfirmasi pesanan</li>
</ol>
```

### 6. Link dan Gambar

```html
<a href="https://instagram.com/">Instagram UMKM</a>

<img src="images/menu.jpg" alt="Foto menu makanan">
```

- `href` — tujuan link (website lain, halaman lain, WhatsApp, atau bagian halaman).
- `src` — lokasi file gambar.
- `alt` — teks alternatif; penting untuk aksesibilitas dan saat gambar gagal dimuat.

### 7. Contoh Proyek: Profil UMKM

Contoh lengkap di modul menggabungkan `h1`, `p`, `ul`, `li`, `a`, dan `href` menjadi satu halaman profil UMKM (nama usaha, deskripsi, daftar menu + harga, dan link WhatsApp).

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `DAWET_Meeting_02_HTML_Dasar_Modul.pdf` | Modul bacaan lengkap (versi final) |
| `DAWET_Meeting_02_HTML_Dasar_Modul.tex` | Sumber LaTeX modul |
| `DAWET_Meeting_02_HTML_Dasar_Modern.pptx` | Slide presentasi pertemuan |
| `index.html` | Demo halaman: `header`, `nav`, `main`, gambar, list, tabel |
| `index2.html` | Demo lengkap dengan komentar penjelas tiap tag: `head`, `header`, `main`, `footer`, list, tabel |
| `latihan/index.html` | Halaman latihan dengan Bootstrap + tabel jadwal |
| `latihan/about.html`, `blog.html`, `contact.html` | Halaman latihan multi-page |
| `img1.jpg` | Aset gambar untuk `index2.html` |
| `referensi.jpg` | Aset gambar untuk `index.html` |
| `latihan/img/hehe.jpg` | Ikon/favicon untuk halaman latihan |

**Catatan:**

- `index2.html` paling berguna untuk dibaca berurutan karena setiap tag diberi komentar penjelas.
- Tabel dibahas di demo (`index2.html`, `latihan/index.html`) sebagai pengayaan, meskipun bukan fokus utama modul.
- `index.html` juga menautkan halaman Kontak dari folder `latihan/` sebagai contoh link antar folder.

---

## Praktik & Tugas

Buat halaman **profil UMKM** dengan ketentuan:

1. Satu judul utama menggunakan `<h1>`.
2. Deskripsi singkat menggunakan `<p>`.
3. Minimal tiga menu menggunakan `<ul>` dan `<li>`.
4. Satu gambar menggunakan `<img>` dan `alt`.
5. Satu link kontak menggunakan `<a>` dan `href`.
6. Struktur `html`, `head`, dan `body` yang benar.

**Tantangan tambahan:**

- Link Instagram.
- Daftar langkah pemesanan menggunakan `<ol>`.
- Harga untuk setiap menu.
- Komentar HTML untuk menandai bagian kode.
- Judul halaman yang sesuai pada `<title>`.

**Tugas GitHub:** simpan proyek di repository pribadi dan tambahkan README berisi identitas, judul proyek, deskripsi, teknologi, hal yang dipelajari, kendala & solusi, serta screenshot.

---

## Checkpoint Pemahaman

1. Apa fungsi HTML?
2. Apa perbedaan tag, element, dan attribute?
3. Apa fungsi `href` dan `src`?
4. Kapan menggunakan `ul` dan kapan menggunakan `ol`?
5. Apa perbedaan `head` dan `body`?
6. Mengapa gambar sebaiknya memiliki attribute `alt`?

---

## Referensi

- MDN — [Basic HTML syntax](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Basic_HTML_syntax)
- MDN — [HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
- W3C — [Markup Validation Service](https://validator.w3.org/)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 01 — Pengenalan HTML](../01-pengenalan-html/README.md) | [Modul 03 — HTML Lanjutan](../03-html-lanjutan/README.md) |
