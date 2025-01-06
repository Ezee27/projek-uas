# Program Data Mahasiswa

Program ini adalah aplikasi sederhana untuk mengelola data mahasiswa menggunakan **konsep modular** dan **OOP (Object-Oriented Programming)**. Program ini memungkinkan pengguna untuk menambahkan data mahasiswa, menampilkan data mahasiswa dalam bentuk tabel, serta memvalidasi input untuk memastikan data yang dimasukkan benar.

---

![Gambar WhatsApp 2025-01-03 pukul 02 40 17_541fdf1e](https://github.com/user-attachments/assets/c84b1d08-f2c1-4de7-adfc-e41fc129b276)


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

    ![DATA](https://github.com/user-attachments/assets/a4416e4b-e4a1-48a2-adcf-b33d62b47f93)


2. **`view.py`**
   - Berinteraksi dengan pengguna (input/output) melalui class `ViewMahasiswa`.
   - Fungsi utama:
     - `tampilkan_menu`: Menampilkan menu utama.
     - `minta_input`: Meminta input dari pengguna.
     - `tampilkan_data`: Menampilkan data mahasiswa dalam format tabel.

   ![VIEW](https://github.com/user-attachments/assets/8ce84fef-7899-4fab-8947-672645266ce1)


3. **`process.py`**
   - Memproses dan memvalidasi input dengan class `ProcessMahasiswa`.
   - Fungsi utama:
     - `validasi_nim`: Memvalidasi NIM (harus angka positif).
     - `validasi_umur`: Memvalidasi umur (harus angka positif).
     - `validasi_nilai`: Memvalidasi nilai (harus dalam rentang 0-100).

![PROCESS](https://github.com/user-attachments/assets/70ce34c7-d290-428d-b38d-9d3349e00024)


4. **`main.py`**
   - Entry point untuk menjalankan program.
   - Mengintegrasikan semua modul (`data.py`, `view.py`, `process.py`).

![MAIN](https://github.com/user-attachments/assets/9ee00033-441b-4059-a565-a66581be45c7)

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
![Screenshot (111)](https://github.com/user-attachments/assets/5b475a21-6f4b-46ec-bd17-e058f3ef5d1a)

### Tambah Data Mahasiswa
```plaintext
Masukkan nama: John Doe
Masukkan NIM: 123456
Masukkan umur: 21
Masukkan nilai: 85
Data mahasiswa berhasil ditambahkan!
```
![Screenshot (112)](https://github.com/user-attachments/assets/38437a09-8fc6-4d7c-9545-634e32fced4c)


### Tampilkan Data Mahasiswa
```plaintext
=== Data Mahasiswa ===
Nama                 NIM             Umur       Nilai     
------------------------------------------------------------
John Doe             123456          21         85.0      
------------------------------------------------------------
```
![image](https://github.com/user-attachments/assets/68ea9896-bf83-4d8e-9e94-33c2890f9710)


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
