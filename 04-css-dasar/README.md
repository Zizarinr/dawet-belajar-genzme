# Modul 04 — CSS Dasar

**Fase 1 · Web Foundation · Pertemuan 4**

> HTML menentukan *apa* yang ada di halaman; CSS menentukan *bagaimana* elemen tersebut terlihat.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan perbedaan peran HTML dan CSS.
2. Membaca aturan dasar CSS.
3. Membuat `style.css` dan menghubungkannya ke HTML.
4. Menggunakan selector elemen, class, dan ID.
5. Mengatur warna, latar, font, dan perataan teks.
6. Memahami `margin`, `padding`, dan `border`.
7. Mencoba perubahan dan memeriksa kesalahan sederhana.

> Flexbox, Grid, responsive design, dan animasi sengaja ditunda ke modul berikutnya agar fondasi CSS tidak dipelajari terburu-buru.

---

## Ringkasan Materi

### 1. Cara Kerja CSS

```css
p {
    color: blue;
    font-size: 18px;
}
```

- **Selector** — `p`, memilih elemen yang akan diberi gaya.
- **Property** — `color`, `font-size`, hal yang diatur.
- **Value** — `blue`, `18px`, nilai yang diberikan.

### 2. Tiga Cara Menambahkan CSS

| Cara | Penempatan | Kapan dipakai |
|------|------------|---------------|
| Inline | `style="..."` pada tag | Uji cepat, hindari untuk proyek nyata |
| Internal | `<style>` di dalam `<head>` | Halaman tunggal |
| External | `<link rel="stylesheet" href="style.css">` | **Direkomendasikan** untuk proyek |

```html
<link rel="stylesheet" href="style.css">
```

Perhatikan path `href` — jika CSS berada di folder `css/`, tulis `href="css/style.css"`.

### 3. Selector

| Jenis | Contoh | Keterangan |
|-------|--------|-----------|
| Element | `h1 { ... }` | Semua elemen `h1` |
| Class | `.menu { ... }` | Semua elemen dengan `class="menu"`; boleh dipakai berulang |
| ID | `#header { ... }` | Satu elemen unik dengan `id="header"` |

### 4. Warna dan Latar

```css
body {
    background-color: #29a284;
    color: #030303;
}
```

### 5. Teks dan Tipografi

```css
h1 {
    font-size: 2rem;
    font-family: Arial, sans-serif;
    text-align: center;
}
```

### 6. Margin, Padding, dan Border (Box Model)

```
┌─────────────────────────────┐
│           margin            │
│  ┌───────────────────────┐  │
│  │        border         │  │
│  │  ┌─────────────────┐  │  │
│  │  │     padding     │  │  │
│  │  │  ┌───────────┐  │  │  │
│  │  │  │  content  │  │  │  │
│  │  │  └───────────┘  │  │  │
│  │  └─────────────────┘  │  │
│  └───────────────────────┘  │
└─────────────────────────────┘
```

| Properti | Fungsi |
|----------|--------|
| `padding` | Jarak di dalam elemen (antara konten dan border) |
| `border` | Garis tepi elemen |
| `margin` | Jarak di luar elemen (antar elemen) |

### 7. Ukuran Elemen dan Gambar

Atur lebar/tinggi gambar secara eksplisit bila perlu, dan gunakan `display: block` + `margin: auto` untuk memusatkan elemen.

### 8. Styling Navigasi

```css
.menu {
    list-style-type: none;
    padding: 0;
    text-align: center;
}

.menu li {
    display: inline-block;
    margin: 0 10px;
}

.menu a {
    text-decoration: none;
    font-weight: bold;
}
```

### 9. Jika CSS Tidak Berhasil

Periksa berurutan: file sudah disimpan → browser di-refresh → nama file `style.css` benar → path `href` sesuai → selector cocok dengan class/id di HTML → kurung kurawal, titik dua, dan titik koma benar → ubah satu hal kecil sekaligus.

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `DAWET_Week_04_CSS_Dasar_Modul_Rinci.pdf` | Modul bacaan lengkap |
| `DAWET_Week_04_CSS_Dasar_Modul_Rinci.tex` | Sumber LaTeX modul |
| `DAWET_Week_04_CSS_Dasar_Modern.pptx` | Slide presentasi |
| `codingan-na/index.html` | Halaman latihan yang sudah memakai CSS eksternal dan class |
| `codingan-na/style.css` | Contoh CSS: warna, tipografi, menu horizontal, box model, tabel |
| `codingan-na/img1.jpg`, `giphy.gif` | Aset gambar |
| `codingan-na/contact.html`, `info_pribadi.html` | Halaman pendukung navigasi |

`codingan-na/` adalah hasil akhir yang bisa dibandingkan dengan `03-html-lanjutan/` untuk melihat apa yang berubah setelah CSS ditambahkan.

---

## Praktik Terpandu

1. Gunakan project dari Modul 03.
2. Buat file `style.css` di folder proyek.
3. Hubungkan dengan `<link rel="stylesheet" href="style.css">`.
4. Tulis aturan pertama: warna latar dan font body.
5. Tambahkan kartu produk (class) dan beri padding, border, serta radius.
6. Beri gaya pada navigasi: hilangkan bullet, susun horizontal.
7. Eksperimen satu perubahan, amati hasilnya, lalu lanjut.

---

## Tugas Mandiri

Lanjutkan Portal UMKM dari Modul 03:

1. Hubungkan `style.css` ke seluruh halaman.
2. Tentukan dua atau tiga warna yang konsisten.
3. Atur font dan ukuran judul/paragraf.
4. Rapikan jarak dengan `margin` dan `padding`.
5. Tambahkan border pada satu bagian yang sesuai.
6. Gunakan satu class pada lebih dari satu elemen.
7. Tulis di README: "Apa yang berubah setelah menggunakan CSS?"
8. Commit dan push ke GitHub.

---

## Checkpoint

- [ ] Bisa menjelaskan perbedaan HTML dan CSS.
- [ ] Paham selector, property, dan value.
- [ ] Bisa membuat dan menghubungkan `style.css`.
- [ ] Bisa membedakan selector tag, class, dan ID.
- [ ] Bisa mengubah warna, latar, ukuran, dan perataan teks.
- [ ] Bisa menjelaskan perbedaan `margin` dan `padding`.
- [ ] Bisa memakai `border`.
- [ ] Bisa menemukan setidaknya satu kesalahan CSS sederhana.

---

## Referensi

- MDN — [CSS styling basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics)
- MDN — [CSS reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- W3C — [CSS Validator](https://jigsaw.w3.org/css-validator/)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 03 — HTML Lanjutan](../03-html-lanjutan/README.md) | [Modul 05 — CSS Layout](../05-css-layout-flexbox-grid/README.md) |
