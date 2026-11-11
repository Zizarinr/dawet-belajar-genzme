# Modul 08 — JavaScript Dasar

**Fase 1 · Web Foundation · Pertemuan 8**

> Variabel menyimpan data, operator memproses nilai, percabangan mengambil keputusan, perulangan mengulang tugas, fungsi merapikan kode.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan peran JavaScript dalam website.
2. Menambahkan JavaScript ke halaman HTML dan memakai console.
3. Membuat variabel serta memahami tipe data dasar.
4. Menggunakan operator aritmatika, perbandingan, dan logika.
5. Membuat percabangan dan perulangan.
6. Membuat fungsi dengan parameter dan `return`.
7. Mengolah array dan object sederhana.

---

## Ringkasan Materi

### 1. Peran JavaScript

| Teknologi | Peran |
|-----------|-------|
| HTML | Struktur dan konten |
| CSS | Tampilan |
| JavaScript | Logika dan interaksi |

JavaScript dapat ditambahkan lewat `<script src="script.js"></script>` sebelum `</body>`, atau langsung di dalam `<script>`.

```javascript
console.log("Hello, DAWET!");
```

Console (buka **DevTools → Console**) dipakai untuk melihat hasil program dan membantu *debugging*.

### 2. Variabel dan Tipe Data

```javascript
let total = 0;        // bisa diubah
const nama = "DAWET"; // tidak bisa di-reassign
```

| Tipe | Contoh |
|------|--------|
| String | `"Kopi Susu"` |
| Number | `15000` |
| Boolean | `true` / `false` |
| Array | `["HTML", "CSS"]` |
| Object | `{ nama: "Kopi", harga: 15000 }` |

Gunakan `typeof` untuk memeriksa tipe data.

### 3. Operator

```javascript
// Aritmatika
10 + 5;  10 - 5;  10 * 5;  10 / 5;  10 % 3;

// Perbandingan (gunakan === dan !==)
10 === 10;  10 !== 5;  10 > 5;  10 <= 5;

// Logika
true && false;  true || false;  !true;
```

`===` membandingkan nilai **dan** tipe, sehingga lebih aman daripada `==`.

### 4. Percabangan

```javascript
if (totalBelanja >= 50000) {
    console.log("Selamat, Anda mendapat diskon!");
} else if (totalBelanja >= 30000) {
    console.log("Hampir dapat diskon.");
} else {
    console.log("Belum memenuhi syarat diskon.");
}

switch (hari) {
    case "Senin":
        console.log("Awal minggu");
        break;
    default:
        console.log("Hari biasa");
}
```

### 5. Perulangan

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}

let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

`break` menghentikan perulangan; `continue` melewati iterasi saat ini.

### 6. Fungsi

```javascript
function hitungTotal(harga, jumlah) {   // function declaration
    return harga * jumlah;
}

const hitungTotal2 = function (harga, jumlah) {  // function expression
    return harga * jumlah;
};

const hitungTotal3 = (harga, jumlah) => harga * jumlah; // arrow function
```

**Parameter** adalah variabel di definisi fungsi; **argument** adalah nilai yang dikirim saat pemanggilan.

### 7. Array

```javascript
const produk = ["Kopi", "Roti", "Teh"];

produk[0];        // "Kopi" — index dimulai dari 0
produk.length;    // 3
produk.push("Susu");
produk.pop();
produk.forEach((item) => console.log(item));
```

### 8. Object

```javascript
const produk = {
    nama: "Kopi Susu",
    harga: 15000,
    stok: 10
};

produk.nama;        // "Kopi Susu"
produk["harga"];    // 15000
produk.stok = 8;    // mengubah properti
```

**Array of objects** dipakai untuk menyimpan banyak data terstruktur, misalnya daftar produk.

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `Pertemuan 8 - JavaScript.pdf` | Modul bacaan lengkap |
| `Pertemuan_8.tex` | Sumber LaTeX modul |

Folder ini hanya berisi materi bacaan; kode praktik dibuat sendiri sebagai `script.js`.

---

## Praktik Terpadu: Sistem Perhitungan Belanja

Buat `script.js` berisi data produk, lalu hitung total belanja dan tentukan diskon.

```javascript
const daftarProduk = [
    { nama: "Kopi Susu", harga: 15000, jumlah: 2 },
    { nama: "Roti Bakar", harga: 12000, jumlah: 1 },
    { nama: "Teh Manis", harga: 8000, jumlah: 3 }
];

function hitungTotal(harga, jumlah) {
    return harga * jumlah;
}

let totalBelanja = 0;

console.log("DAFTAR BELANJA");

for (const produk of daftarProduk) {
    const subtotal = hitungTotal(produk.harga, produk.jumlah);
    totalBelanja += subtotal;
    console.log(produk.nama + ": Rp" + subtotal);
}

console.log("----------------");
console.log("Total: Rp" + totalBelanja);

if (totalBelanja >= 50000) {
    console.log("Selamat, Anda mendapat diskon!");
} else {
    console.log("Belum memenuhi syarat diskon.");
}
```

Program ini menggabungkan **array of objects**, **fungsi**, **perulangan**, **variabel**, **operator**, dan **percabangan**. Hubungkan `script.js` ke HTML, buka halaman, lalu lihat hasilnya di tab Console.

---

## Latihan Mandiri

1. **Variabel & operator** — buat variabel nama toko, nama produk, harga, jumlah; hitung total dan tampilkan dengan `console.log()`.
2. **Percabangan** — tentukan pesan berdasarkan `stok`: `> 0` → "Produk tersedia", `0` → "Produk habis", `< 0` → "Data stok tidak valid".
3. **Perulangan** — buat array minimal lima nama produk, tampilkan semuanya ke console.
4. **Fungsi** — buat `hitungDiskon(harga, persentase)` yang mengembalikan harga setelah diskon. Contoh: `hitungDiskon(100000, 10)` → `90000`.
5. **Object & array** — buat `daftarProduk` berisi minimal tiga object (`nama`, `harga`, `stok`), lalu tampilkan nama, harga, total stok, dan produk yang stoknya lebih dari nol.

---

## Evaluasi Pemahaman

1. Apa perbedaan `let` dan `const`?
2. Apa perbedaan tipe data String, Number, dan Boolean?
3. Mengapa `===` lebih disarankan daripada `==`?
4. Kapan menggunakan percabangan `if-else`?
5. Apa perbedaan perulangan `for` dan `while`?
6. Apa perbedaan parameter dan argument?
7. Mengapa index array dimulai dari nol?
8. Apa perbedaan array dan object?
9. Mengapa array of objects berguna untuk menyimpan data produk?
10. Jelaskan cara kerja program perhitungan belanja pada modul ini.

**Kriteria penyelesaian:** mampu membuat file JS eksternal dan menghubungkannya ke HTML, memakai console, membuat variabel dan tipe data dasar, memakai operator, percabangan, perulangan, fungsi dengan parameter & return, serta mengolah array dan object tanpa sekadar menyalin contoh.

---

## Referensi

- MDN — [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- MDN — [JavaScript First Steps](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting)
- MDN — [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [javascript.info](https://javascript.info/)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 07 — Git & GitHub](../07-git-github-dokumentasi/README.md) | — (akhir Fase 1) |
