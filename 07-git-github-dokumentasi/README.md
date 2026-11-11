# Modul 07 — Git, GitHub & Dokumentasi Proyek

**Fase 1 · Web Foundation · Pertemuan 7**

> Menyimpan proyek bukan hanya di folder lokal, tetapi juga mencatat riwayatnya dan mendokumentasikannya.

---

## Tujuan Pembelajaran

Setelah menyelesaikan materi ini, peserta diharapkan mampu:

1. Menjelaskan perbedaan Git dan GitHub.
2. Memahami konsep repository, commit, staging, dan remote repository.
3. Menginstal serta melakukan konfigurasi dasar Git.
4. Membuat repository di GitHub.
5. Menghubungkan proyek lokal dengan repository GitHub.
6. Mengunggah perubahan proyek menggunakan Git.
7. Menyusun dokumentasi proyek menggunakan `README.md`.

---

## Ringkasan Materi

### 1. Git vs GitHub

| Aspek | Git | GitHub |
|-------|-----|--------|
| Bentuk | Software version control | Platform hosting repository |
| Penggunaan | Mengelola riwayat perubahan | Menyimpan & membagikan repository |
| Koneksi internet | Bisa dipakai lokal | Butuh internet |
| Contoh aktivitas | Commit, branch, merge | Membuat repository, Pull Request |

**Git** mencatat setiap perubahan file proyek. **GitHub** adalah tempat penyimpanan daring untuk repository Git — bukan pengganti Git.

### 2. Konsep Dasar

| Istilah | Arti |
|---------|------|
| **Repository** | Tempat penyimpanan proyek beserta riwayat perubahannya. Bisa *local* atau *remote* |
| **Working directory** | Folder tempat kita mengedit file |
| **Staging area** | Area sementara untuk memilih perubahan yang akan di-commit |
| **Commit** | Catatan perubahan dengan identitas unik dan pesan |
| **Remote** | Referensi ke repository lain (GitHub) |
| **Branch** | Jalur pengembangan terpisah; tahap awal memakai `main` |

### 3. Persiapan

```bash
git --version

git config --global user.name "Nama Kamu"
git config --global user.email "email@example.com"
git config --global --list
```

Konfigurasi identitas Git **tidak** otomatis melakukan autentikasi ke akun GitHub.

### 4. Membuat Repository di GitHub

1. Buka <https://github.com/> dan login.
2. Klik **New**.
3. Isi nama repository, misalnya `dawet-assignment-1-nama`.
4. Tambahkan deskripsi singkat.
5. Pilih visibilitas sesuai kebutuhan.
6. Untuk latihan, buat repository **kosong** (tanpa README, `.gitignore`, atau lisensi).
7. Klik **Create repository**.

> **Perhatian:** repository Public dapat dilihat siapa saja. Jangan pernah mengunggah kata sandi, API key, token, atau data pribadi.

### 5. Menghubungkan Proyek Lokal ke GitHub

```bash
cd Documents/website-umkm   # masuk ke folder proyek

git init                    # inisialisasi repository lokal
git status                  # cek kondisi repository
git add .                   # masukkan perubahan ke staging area
git commit -m "Initial commit"
git branch -M main          # pastikan branch utama bernama main

git remote add origin https://github.com/username/nama-repository.git
git remote -v

git push -u origin main
```

Opsi `-u` mengatur upstream branch, sehingga berikutnya cukup menjalankan `git push`.

### 6. Alur Kerja Harian

```
ubah file → git status → git add . → git commit -m "..." → git push
```

Contoh:

```bash
git status
git add .
git commit -m "Memperbaiki tampilan halaman utama"
git push
```

**Pesan commit yang baik** menjelaskan perubahan secara spesifik:

- ✅ `Menambahkan halaman produk`
- ✅ `Memperbaiki navigasi website`
- ✅ `Mengatur layout kartu produk`
- ❌ `Update`, `Perbaikan`, `Final`

### 7. README.md

README adalah dokumen pengantar proyek, otomatis tampil di halaman utama repository GitHub. Format `.md` (Markdown) mendukung judul, paragraf, daftar, tautan, dan gambar.

Struktur README sederhana:

```markdown
# Website UMKM

Website sederhana untuk memperkenalkan produk dan informasi UMKM.

## Deskripsi
Proyek ini dibuat sebagai bagian dari Assignment 1 Project DAWET.

## Fitur
- Halaman utama
- Halaman profil UMKM
- Daftar produk
- Informasi kontak

## Teknologi
- HTML
- CSS

## Struktur Proyek
website-umkm/
├── index.html
├── tentang.html
├── produk.html
├── kontak.html
├── css/
└── images/

## Cara Menjalankan
1. Clone repository.
2. Buka folder proyek.
3. Jalankan `index.html` melalui browser.

## Pengembang
Nama: Nama Peserta
Program: Project DAWET
```

Simpan `README.md` sejajar dengan `index.html`, lalu:

```bash
git add README.md
git commit -m "Menambahkan dokumentasi proyek"
git push
```

### 8. Kendala Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|---------|----------|--------|
| `'git' is not recognized` | Git belum terinstal / belum masuk PATH | Instal Git, buka ulang terminal, cek `git --version` |
| `Author identity unknown` | Nama/email belum dikonfigurasi | `git config --global user.name` dan `user.email` |
| `remote origin already exists` | Remote `origin` sudah terdaftar | Cek `git remote -v`; perbaiki dengan `git remote set-url origin URL` |
| `! [rejected] main -> main (fetch first)` | Riwayat lokal & remote berbeda | Hindari repo GitHub berisi README saat awal; **jangan** langsung `push --force` |
| File tidak muncul di GitHub | Belum di-add/commit/push, atau URL salah | Cek `git status`, `git remote -v`, `git log --oneline` |

---

## File di Folder Ini

| File | Keterangan |
|------|------------|
| `Pertemuan 7 - Github & Dokumentasi.pdf` | Modul bacaan lengkap |

Folder ini hanya berisi materi bacaan; praktik dilakukan pada proyek HTML/CSS masing-masing.

---

## Praktik Mandiri

1. Siapkan proyek HTML & CSS dari modul sebelumnya.
2. Rapikan struktur folder proyek.
3. Buat repository baru di GitHub.
4. Hubungkan proyek lokal dengan repository tersebut.
5. Unggah seluruh file proyek.
6. Buat `README.md`.
7. Lakukan minimal dua commit dengan pesan yang jelas.
8. Pastikan semua perubahan muncul di GitHub.

**Ketentuan:** repository dapat diakses untuk pemeriksaan, nama repository jelas, README sesuai kondisi proyek, tidak ada file rahasia, dan seluruh aset dapat ditemukan.

**Checklist:**

- [ ] Git terinstal
- [ ] Identitas Git dikonfigurasi
- [ ] Repository GitHub dibuat
- [ ] Proyek lokal terhubung ke GitHub
- [ ] File proyek berhasil diunggah
- [ ] `README.md` dibuat
- [ ] Minimal dua commit
- [ ] Repository dapat dibuka dan diperiksa

---

## Hubungan dengan Assignment 1

Modul ini menutup rangkaian **Assignment 1: Web Foundation**. Penilaian tidak hanya melihat tampilan website, tetapi juga kerapian repository, riwayat commit, kualitas README, dan kemampuan menjelaskan pekerjaan.

| Aspek | Indikator |
|-------|-----------|
| Repository | Tersedia dan dapat diakses |
| Struktur | File proyek tersusun jelas |
| Commit | Riwayat terlihat dengan pesan relevan |
| README | Dokumentasi menjelaskan proyek dengan benar |
| Pemahaman | Mampu menjelaskan Git, GitHub, dan alur kerjanya |

---

## Referensi

- [Git Documentation](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [GitHub Docs](https://docs.github.com/)
- [About Git — GitHub](https://docs.github.com/en/get-started/using-git/about-git)
- [Creating a Repository — GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)
- [GitHub Hello World](https://docs.github.com/en/get-started/start-your-journey/hello-world)

---

## Navigasi

| ← Sebelumnya | Berikutnya → |
|:---|:---|
| [Modul 06 — Responsive Web Design](../06-responsive-web-design/README.md) | [Modul 08 — JavaScript Dasar](../08-javascript-dasar/README.md) |
