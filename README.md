# Pertemuan 09 - List dan Pengolahan Data Numerik

- **Nama**: Dita Amalia Veronica
- **NIM**: 2225250162
- **Kelas**: 3F

---

## Tujuan
Mengolah kumpulan data numerik menggunakan list/array Python, melakukan akses dan manipulasi elemen, penelusuran data dengan perulangan, serta mengimplementasikannya dalam fungsi statistik sederhana.

---

## Struktur Program

| Jenis File | Nama File / Folder | Keterangan Program |
| :--- | :--- | :--- |
| **Dokumentasi** | `README.md` | Catatan petunjuk, test case, dan refleksi[cite: 5] |
| **Pengaturan** | `.gitignore` | Mengabaikan file temporary / cache[cite: 5] |
| **Latihan 1** | `latihan/01_buat_list.py` | Membuat list numerik dan menghitung jumlah elemen dengan `len()`[cite: 5, 9] |
| **Latihan 2** | `latihan/02_indeks_slicing.py` | Akses elemen menggunakan indeks positif, negatif, dan slicing[cite: 5, 9] |
| **Latihan 3** | `latihan/03_manipulasi_list.py` | Mengubah elemen, `append()`, `insert()`, dan `remove()`[cite: 5, 9] |
| **Latihan 4** | `latihan/04_agregasi_nilai.py` | Menghitung `sum()`, rata-rata, `min()`, dan `max()`[cite: 5, 10] |
| **Latihan 5** | `latihan/05_filter_kelulusan.py` | Menyaring nilai lulus (`>= 60`) dan memasukkannya ke list baru[cite: 5, 10] |
| **Latihan 6** | `latihan/06_fungsi_statistik.py` | Fungsi hitung rata-rata dengan penanganan list kosong[cite: 5, 10] |
| **Praktik Utama** | `praktik/analisis_nilai_mahasiswa.py` | Program analisis nilai lengkap dan status kelulusan[cite: 5, 11] |

---

## Cara Menjalankan

Jalankan program melalui terminal VS Code dengan perintah berikut:

1. **Menjalankan Latihan:**
   - `python latihan/01_buat_list.py`
   - `python latihan/02_indeks_slicing.py`
   - `python latihan/03_manipulasi_list.py`
   - `python latihan/04_agregasi_nilai.py`
   - `python latihan/05_filter_kelulusan.py`
   - `python latihan/06_fungsi_statistik.py`

2. **Menjalankan Praktik Utama:**
   - `python praktik/analisis_nilai_mahasiswa.py`

---

## Hasil Pengujian (Test Case)

### 1. Pengujian File Latihan (`latihan/`)

| Program | Data Input | Komponen Diuji | Hasil Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **Latihan 1** | `[75, 80, 65, 90, 88]` | Banyak elemen (`len`) | `5` | `5` | **Sesuai** |
| **Latihan 2** | `[75, 80, 65, 90, 88, 70]` | Indeks awal `[0]` & akhir `[-1]` | `75` dan `70` | `75` dan `70` | **Sesuai** |
| **Latihan 2** | `[75, 80, 65, 90, 88, 70]` | Slicing `[:3]` & `[1:4]` | `[75, 80, 65]` & `[80, 65, 90]` | `[75, 80, 65]` & `[80, 65, 90]` | **Sesuai** |
| **Latihan 3** | `[75, 80, 65]` | Manipulasi list (`append`, `insert`, `remove`) | `[75, 70, 82, 90]` | `[75, 70, 82, 90]` | **Sesuai** |
| **Latihan 4** | `[75, 80, 65, 90, 88]` | Total, Rata-rata, Min, Max | `Total: 398, Mean: 79.60, Min: 65, Max: 90` | `Total: 398, Mean: 79.60, Min: 65, Max: 90` | **Sesuai** |
| **Latihan 5** | `[75, 55, 80, 60, 45, 90]` | Filter Kelulusan (`>= 60`) | `Nilai: [75, 80, 60, 90] (4 Lulus)` | `Nilai: [75, 80, 60, 90] (4 Lulus)` | **Sesuai** |
| **Latihan 6** | `[75, 80, 65, 90, 88]` | Fungsi Rata-rata | `79.60` | `79.60` | **Sesuai** |
| **Latihan 6** | `[]` | List Kosong | `0` (Tidak Error) | `0` | **Sesuai** |

### 2. Pengujian Program Utama (`praktik/analisis_nilai_mahasiswa.py`)

| Kasus Uji | Data Input | Parameter Diuji | Hasil Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **Data Utama** | `[78, 55, 90, 67, 60, 82, 45, 71, 88, 59]` | Total & Rata-rata | `Total: 695, Rata-rata: 69.50` | `Total: 695, Rata-rata: 69.50` | **Sesuai** |
| **Data Utama** | `[78, 55, 90, 67, 60, 82, 45, 71, 88, 59]` | Min & Max | `Min: 45, Max: 90` | `Min: 45, Max: 90` | **Sesuai** |
| **Data Utama** | `[78, 55, 90, 67, 60, 82, 45, 71, 88, 59]` | Jumlah Lulus (≥60) | `7 Lulus` | `7 Lulus` | **Sesuai** |
| **Data Utama** | `[78, 55, 90, 67, 60, 82, 45, 71, 88, 59]` | Jumlah Belum Lulus | `3 Belum Lulus` | `3 Belum Lulus` | **Sesuai** |
| **Test Case Wajib** | `[60, 70, 80]` | Rata-rata | `70.00` | `70.00` | **Sesuai** |
| **Test Case Wajib** | `[60, 70, 80]` | Minimum / Maksimum | `60 / 80` | `60 / 80` | **Sesuai** |
| **Test Case Wajib** | `[60, 70, 80]` | Jumlah Lulus | `3` | `3` | **Sesuai** |
| **Test Case Wajib** | `[59, 60, 61]` | Batas Kelulusan | `2 Lulus` | `2 Lulus` | **Sesuai** |
| **Test Case Wajib** | `[]` | List Kosong | `0.00` (Aman / Tidak Error) | `0.00` | **Sesuai** |

---

## Refleksi Praktik

| Topik Refleksi | Penjelasan |
| :--- | :--- |
| **Konsep Paham** | Indeks list Python dimulai dari `0`, dan penggunaan indeks negatif (`-1`) sangat memudahkan pengaksesan elemen paling belakang tanpa perlu menghitung panjang list secara manual. |
| **Perbaikan Kesalahan** | Pentingnya memeriksa panjang list (`len(data) == 0`) sebelum melakukan pembagian saat menghitung nilai rata-rata agar program terhindar dari `ZeroDivisionError`. |