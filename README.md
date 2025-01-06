# Program Data Mahasiswa

Program ini adalah aplikasi sederhana untuk mengelola data mahasiswa menggunakan **konsep modular** dan **OOP (Object-Oriented Programming)**. Program ini memungkinkan pengguna untuk menambahkan data mahasiswa, menampilkan data mahasiswa dalam bentuk tabel, serta memvalidasi input untuk memastikan data yang dimasukkan benar.

---

## Table of Contents
- [Fitur Utama](#fitur-utama)
- [Struktur Program](#struktur-program)
- [Cara Menjalankan](#cara-menjalankan)
- [Contoh Output](#contoh-output)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Lisensi](#lisensi)

---

## Fitur Utama

1. **Tambah Mahasiswa**
   - Input: Nama, NIM, Umur, dan Nilai.
   - Validasi input:
     - Nama: Tidak boleh kosong.
     - NIM: Harus berupa angka positif.
     - Umur: Harus berupa angka positif.
     - Nilai: Harus dalam rentang 0-100.

2. **Tampilkan Data Mahasiswa**
   - Menampilkan data mahasiswa dalam format tabel.
   - Kolom: Nama, NIM, Umur, Nilai.

3. **Keluar**
   - Menghentikan program.

---

## Struktur Program

Program ini dibagi menjadi empat file utama untuk mendukung modularitas:

1. **`data.py`**
   - Mengelola data mahasiswa dengan class `DataMahasiswa`.
   - Fungsi utama:
     - `tambah_mahasiswa`: Menambahkan data mahasiswa ke dalam daftar.
     - `dapatkan_semua_data`: Mengambil semua data mahasiswa.

2. **`view.py`**
   - Berinteraksi dengan pengguna (input/output) melalui class `ViewMahasiswa`.
   - Fungsi utama:
     - `tampilkan_menu`: Menampilkan menu utama.
     - `minta_input`: Meminta input dari pengguna.
     - `tampilkan_data`: Menampilkan data mahasiswa dalam format tabel.

3. **`process.py`**
   - Memproses dan memvalidasi input dengan class `ProcessMahasiswa`.
   - Fungsi utama:
     - `validasi_nim`: Memvalidasi NIM (harus angka positif).
     - `validasi_umur`: Memvalidasi umur (harus angka positif).
     - `validasi_nilai`: Memvalidasi nilai (harus dalam rentang 0-100).

4. **`main.py`**
   - Entry point untuk menjalankan program.
   - Mengintegrasikan semua modul (`data.py`, `view.py`, `process.py`).

---

## Cara Menjalankan

1. Clone repository ini:
   ```bash
   git clone https://github.com/username/ProgramDataMahasiswa.git
   ```

2. Masuk ke direktori proyek:
   ```bash
   cd ProgramDataMahasiswa
   ```

3. Jalankan program:
   ```bash
   python main.py
   ```

---

## Contoh Output

### Menu Utama
```plaintext
=== Program Data Mahasiswa ===
1. Tambah Mahasiswa
2. Tampilkan Data Mahasiswa
3. Keluar
Pilih menu:
```

### Tambah Data Mahasiswa
```plaintext
Masukkan nama: John Doe
Masukkan NIM: 123456
Masukkan umur: 21
Masukkan nilai: 85
Data mahasiswa berhasil ditambahkan!
```

### Tampilkan Data Mahasiswa
```plaintext
=== Data Mahasiswa ===
Nama                 NIM             Umur       Nilai     
------------------------------------------------------------
John Doe             123456          21         85.0      
------------------------------------------------------------
```

### Validasi Input
- Jika NIM tidak valid:
  ```plaintext
  Masukkan NIM: -123
  Error: NIM harus berupa angka positif.
  ```
- Jika umur tidak valid:
  ```plaintext
  Masukkan umur: -5
  Error: Umur harus lebih besar dari 0.
  ```
- Jika nilai tidak valid:
  ```plaintext
  Masukkan nilai: 105
  Error: Nilai harus berada di antara 0 dan 100.
  ```

---

## Teknologi yang Digunakan

- **Python**: Bahasa pemrograman utama.

---
