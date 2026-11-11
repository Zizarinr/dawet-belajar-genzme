# Modul 06 — Responsive Web Design

**Fase 1 · Web Foundation · Pertemuan 6 · Pra-Assignment 1**

> Satu halaman, nyaman digunakan dari ponsel sampai desktop.

---

## Tujuan Pembelajaran

Setelah mempelajari materi ini, peserta diharapkan mampu:

1. Menjelaskan pengertian dan tujuan Responsive Web Design (RWD).
2. Memahami peran viewport dan meta viewport.
3. Mengenali perbedaan satuan tetap dan relatif.
4. Menggunakan media queries berdasarkan ukuran layar.
5. Membuat layout yang menyesuaikan layar desktop dan ponsel.
6. Menguji website pada beberapa ukuran layar.

---

## Ringkasan Materi

### 1. Apa Itu Responsive Web Design?

RWD adalah pendekatan agar tampilan dan tata letak halaman menyesuaikan ukuran layar atau ruang yang tersedia. Bukan membuat website berbeda untuk setiap perangkat, melainkan **satu halaman** yang beradaptasi melalui aturan CSS.

### 2. Prinsip Dasar

```css
/* Layout fleksibel */
.container {
    width: 90%;
    max-width: 1100px;
    margin: 0 auto;
}

/* Media fleksibel */
img {
    max-width: 100%;
    height: auto;
}
```

Prinsip ketiga: konten mudah dibaca — perhatikan ukuran teks, jarak antar-elemen, dan area sentuh tombol pada layar kecil.

### 3. Viewport dan Meta Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- `width=device-width` — lebar viewport mengikuti lebar perangkat.
- `initial-scale=1.0` — skala awal halaman.

Tanpa meta ini, halaman ponsel bisa ditampilkan dengan skala yang tidak sesuai.

### 4. Satuan CSS

| Satuan | Relatif terhadap | Cocok untuk |
|--------|------------------|-------------|
| `px` | — (tetap) | Detail kecil seperti border |
| `%` | Ukuran elemen induk | Lebar container |
| `rem` | Ukuran font root | Teks dan spacing |
| `vw` | Lebar viewport | Elemen selebar layar |
| `vh` | Tinggi viewport | Bagian setinggi layar |

Tidak semua ukuran harus relatif — pilih berdasarkan kebutuhan.

### 5. Media Queries

```css
@media (max-width: 768px) {
    /* aturan untuk viewport maksimal 768px */
}
```

**Mengubah layout kartu:**

```css
.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .cards {
        grid-template-columns: 1fr;
    }
}
```

**Mengubah navigasi:**

```css
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        align-items: flex-start;
        gap: 12px;
    }
}
```

### 6. Menguji Responsive Design

1. Buka halaman di browser.
2. Tekan `F12` atau klik kanan → **Inspect**.
3. Aktifkan **Device Toolbar**.
4. Pilih ukuran perangkat atau masukkan lebar viewport manual.
5. Amati scroll horizontal, teks terpotong, atau elemen bertumpuk.
6. Periksa kembali layar lebar dan kecil setelah mengubah CSS.

Device Toolbar hanyalah simulasi — uji di perangkat nyata bila memungkinkan.

### 7. Kesalahan yang Sering Terjadi

- Lupa memasang meta viewport.
- Lebar elemen tetap berlebihan sehingga melampaui layar.
- Gambar terlalu besar → muncul scroll horizontal.
- Hanya menguji di desktop.
- Breakpoint tidak diuji; pilih breakpoint saat konten mulai tidak nyaman ditampilkan.

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `DAWET_Minggu_6_Pra_Assignment_1_Responsive_Web_Design.pdf` | Modul bacaan lengkap (termasuk contoh `index.html` dan `style.css` utuh) |

Folder ini hanya berisi materi bacaan. Kode praktik dibuat sendiri mengikuti panduan di modul.

---

## Praktik Langsung

Buat `index.html` dan `style.css` dalam satu folder, dengan struktur:

- `header.navbar` berisi judul dan tiga link navigasi.
- `main.container` berisi `section.intro` dan `section.cards`.
- Tiga `article.card` untuk HTML, CSS, dan JavaScript.

Inti CSS-nya:

```css
* { box-sizing: border-box; }

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 18px 5%;
}

.container {
    width: 90%;
    max-width: 1100px;
    margin: 35px auto;
}

.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .cards { grid-template-columns: 1fr; }
    .navbar { flex-direction: column; align-items: flex-start; gap: 12px; }
    nav { flex-wrap: wrap; }
}
```

Kecilkan lebar jendela browser: kartu berubah menjadi satu kolom dan navbar menjadi vertikal.

---

## Latihan Mandiri

- Pastikan setiap halaman HTML memiliki meta viewport.
- Ubah layout tiga kartu menjadi satu kolom pada lebar maksimal `768px`.
- Buat navbar berubah menjadi vertikal pada layar kecil.
- Pastikan gambar tidak melampaui lebar container.
- Uji pada viewport lebar dan sempit, lalu catat perubahannya.

---

## Evaluasi Pemahaman

1. Apa yang dimaksud dengan Responsive Web Design?
2. Apa fungsi meta viewport?
3. Apa perbedaan penggunaan `px` dan `%` untuk lebar elemen?
4. Apa fungsi media query?
5. Mengapa website perlu diuji pada lebih dari satu ukuran layar?

**Indikator keberhasilan:** mampu menjelaskan tujuan RWD, memahami meta viewport, memakai satuan relatif secara sederhana, membuat media query, serta menguji layout di desktop dan ponsel.

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 05 — CSS Layout](../05-css-layout-flexbox-grid/README.md) | [Modul 07 — Git & GitHub](../07-git-github-dokumentasi/README.md) |
