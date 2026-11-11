# Modul 01 — Pengenalan HTML

**Fase 1 · Web Foundation · Pertemuan 1**

> Folder ini berisi halaman HTML pertama sebagai titik awal perjalanan. Materi bacaan lengkap (PDF/PPTX) belum tersedia untuk pertemuan ini — pembahasan teori HTML Dasar dilanjutkan di [Modul 02 — HTML Dasar](../02-html-dasar/README.md).

---

## Tujuan Pembelajaran

Setelah menyelesaikan modul ini, peserta diharapkan mampu:

1. Menjelaskan fungsi HTML dalam pembuatan website.
2. Menyiapkan tools dasar: browser dan code editor.
3. Membuat file `index.html` pertama dan membukanya di browser.
4. Mengenali bagian `head` dan `body` pada dokumen HTML.

---

## Ringkasan Materi

### 1. Apa Itu HTML?

HTML (*HyperText Markup Language*) adalah bahasa penanda yang menyusun struktur dan makna konten halaman web. HTML **bukan** bahasa pemrograman — ia tidak memiliki logika seperti perulangan atau percabangan. Tugasnya memberi tahu browser bagian mana yang merupakan judul, paragraf, gambar, atau tautan.

### 2. Tools yang Dibutuhkan

| Tools | Fungsi | Rekomendasi |
|-------|--------|-------------|
| Browser | Menampilkan halaman HTML | Chrome, Edge, Firefox |
| Code editor | Menulis dan mengedit kode | Visual Studio Code |
| Ekstensi *Live Server* (opsional) | Auto-reload saat file disimpan | VS Code Marketplace |

Tidak perlu instalasi server, Node.js, atau framework apa pun di tahap ini.

### 3. Struktur Folder Sederhana

```
DAWET/
└── minggu-01/
    └── index.html
```

Nama `index.html` adalah konvensi umum untuk halaman utama sebuah folder.

### 4. Halaman HTML Pertama

Isi file `index.html` pada folder ini:

```html
<!DOCTYPE html>
<html lang="en" style="color-scheme: dark;">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Pertemuan 1</title>
  </head>
  <body>
    Ini adalah halaman index.html
  </body>
</html>
```

Penjelasan singkat:

- `<!DOCTYPE html>` — menandai dokumen sebagai HTML5.
- `<html>` — elemen akar yang membungkus seluruh dokumen.
- `<head>` — informasi halaman (judul, encoding, viewport); tidak tampil di halaman.
- `<body>` — konten yang terlihat oleh pengunjung.

### 5. Melihat Hasilnya

1. Simpan file dengan ekstensi `.html`.
2. Buka file tersebut di browser.
3. Ubah teks di dalam `<body>`, simpan, lalu *refresh* browser (F5).
4. Klik kanan → **Inspect** untuk melihat struktur HTML yang sama dengan yang kamu tulis.

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `index.html` | Halaman HTML pertama: struktur dasar dengan judul dan satu baris teks |

---

## Praktik & Tugas

1. Buat folder baru bernama `minggu-01` di komputer sendiri.
2. Buat file `index.html` dari nol (jangan menyalin mentah-mentah).
3. Isi `<title>` dengan namamu, dan `<body>` dengan perkenalan singkat (2–3 baris).
4. Buka di browser, lalu coba ubah teksnya dan lihat perubahannya.
5. Buka **Inspect** dan temukan elemen `<h1>` atau `<p>` yang kamu tulis.

**Tantangan tambahan:** tambahkan satu heading dan satu paragraf, lalu perhatikan perbedaan tampilannya.

---

## Checkpoint Pemahaman

1. Apa kepanjangan HTML dan apa fungsinya?
2. Apa perbedaan isi `<head>` dan `<body>`?
3. Mengapa file utama biasanya diberi nama `index.html`?
4. Apa yang terjadi jika file disimpan dengan ekstensi `.txt`?

---

## Referensi

- MDN Web Docs — [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- MDN Web Docs — [HTML: HyperText Markup Language](https://developer.mozilla.org/en-US/docs/Web/HTML)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| — (awal kurikulum) | [Modul 02 — HTML Dasar](../02-html-dasar/README.md) |
