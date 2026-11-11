# Modul 05 — CSS Layout: Flexbox & Grid

**Fase 1 · Web Foundation · Pertemuan 5 · Pra-Assignment 1**

> Mengatur posisi dan susunan elemen, bukan sekadar mempercantik halaman.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan alasan penggunaan CSS Layout.
2. Memahami container (elemen induk) dan item (elemen anak).
3. Mengatur elemen satu arah menggunakan Flexbox.
4. Menyusun elemen dalam baris dan kolom menggunakan CSS Grid.
5. Memilih teknik layout sesuai kebutuhan halaman.
6. Menerapkan Flexbox dan Grid pada proyek HTML sederhana.

---

## Ringkasan Materi

### 1. Container dan Item

```html
<div class="container">
    <div class="item">Satu</div>
    <div class="item">Dua</div>
    <div class="item">Tiga</div>
</div>
```

**Container** adalah elemen induk tempat item berkumpul; **item** adalah elemen anak di dalamnya. Ketika Flexbox atau Grid diterapkan pada container, seluruh item mengikuti aturan layout tersebut.

### 2. Flexbox — Satu Dimensi

Flexbox menyusun item dalam satu arah: baris **atau** kolom.

```css
.container {
    display: flex;
    flex-direction: row;      /* row | column | row-reverse | column-reverse */
    justify-content: center;  /* sumbu utama: flex-start | flex-end | center | space-between | space-around | space-evenly */
    align-items: center;      /* sumbu silang */
    gap: 20px;
}
```

- `justify-content` mengatur distribusi pada **main axis**.
- `align-items` mengatur posisi pada **cross axis**.
- Arah kedua sumbu mengikuti `flex-direction`: jika `row`, main axis horizontal; jika `column`, main axis vertikal.

### 3. CSS Grid — Dua Dimensi

Grid menyusun item dalam baris dan kolom sekaligus.

```css
.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

`1fr` berarti satu bagian dari ruang yang tersedia. `repeat(3, 1fr)` menghasilkan tiga kolom sama lebar.

### 4. Flexbox atau Grid?

| Kebutuhan | Pilihan yang sering sesuai |
|-----------|---------------------------|
| Navbar | Flexbox |
| Menyejajarkan tombol | Flexbox |
| Menu horizontal | Flexbox |
| Galeri foto | Grid |
| Daftar produk berbentuk kolom | Grid |
| Dashboard dengan area baris & kolom | Grid |

Keduanya bisa dipakai bersama: Grid membagi halaman menjadi sidebar dan konten utama, lalu Flexbox menyusun tombol di dalam konten.

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `DAWET_Minggu_5_Pra_Assignment_1_CSS_Layout.pdf` | Modul bacaan lengkap |
| `DAWET_Minggu_5_Pra_Assignment_1_CSS_Layout.tex` | Sumber LaTeX modul |

Folder ini hanya berisi materi bacaan. Kode praktik dibuat sendiri mengikuti panduan di bawah.

---

## Praktik Langsung

Buat `layout.html` dan `style.css` dalam satu folder.

**`layout.html`**

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Belajar CSS Layout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="navbar">
        <h2>DAWET</h2>
        <nav>
            <a href="#">Beranda</a>
            <a href="#">Tentang</a>
            <a href="#">Kontak</a>
        </nav>
    </header>
    <main>
        <h1>Belajar CSS Grid</h1>
        <section class="cards">
            <div class="card">HTML</div>
            <div class="card">CSS</div>
            <div class="card">JavaScript</div>
        </section>
    </main>
</body>
</html>
```

**`style.css`**

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav {
    display: flex;
    gap: 20px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.card {
    background: #eeeeee;
    padding: 30px;
    text-align: center;
}
```

Navbar memakai Flexbox, tiga kartu memakai Grid.

---

## Latihan Mandiri

1. Ubah posisi menu navigasi agar berada di sebelah kiri.
2. Buat empat kartu menggunakan Grid.
3. Ubah jarak antarkartu menjadi `30px`.
4. Pastikan logo dan menu tetap sejajar secara vertikal.
5. Ubah `flex-direction` dari `row` menjadi `column`, lalu amati perbedaannya.

---

## Evaluasi Pemahaman

1. Apa perbedaan utama Flexbox dan CSS Grid?
2. Apa fungsi container dan item?
3. Apa perbedaan `justify-content` dan `align-items`?
4. Mengapa Grid cocok untuk galeri foto atau daftar produk?
5. Berikan satu contoh situasi ketika Flexbox dan Grid digunakan bersama.

**Indikator keberhasilan:** mampu menjelaskan perbedaan keduanya, memakai `display: flex` dan `display: grid`, menyusun navbar serta kartu sederhana, dan memodifikasi layout yang sudah ada.

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 04 — CSS Dasar](../04-css-dasar/README.md) | [Modul 06 — Responsive Web Design](../06-responsive-web-design/README.md) |
