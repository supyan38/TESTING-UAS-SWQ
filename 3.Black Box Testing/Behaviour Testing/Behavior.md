# 🧪 Boundary Value Analysis (BVA)

**Model Pengujian Black Box** yang menguji nilai input pada batas minimal dan maksimal untuk memastikan sistem dapat menangani nilai ekstrem dengan benar.

## 🎯 Fitur yang Diuji
- Menambahkan Task Baru (Form Input)

## 🧾 Deskripsi
Dilakukan pengujian terhadap batas input `judul` dan `tanggal` pada form tambah task. Tujuan pengujian ini untuk memastikan sistem memvalidasi nilai minimum, maksimum, dan nilai kosong.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|------------------|----------------|--------|---------------|
| 1 | `A` (1 karakter) | `2025-01-01` | Task berhasil ditambah | Task muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/49c603b6-2aae-41f9-a50c-30f80ed038f6" /> |
| 2 | *(kosong)* | `2025-01-01` | Error: judul tidak boleh kosong | Task tidak ditambah | ✅ | <img width="300" src="https://github.com/user-attachments/assets/b3a6ae87-10e6-4cdf-99e9-8070238f6261" /> |
| 3 | `A...A` (256 karakter) | `2025-01-01` | Error: input terlalu panjang | Tidak diproses | ✅ | <img width="300" src="https://github.com/user-attachments/assets/fcb16619-4886-4ec2-a6aa-82201d6bef3d" /> |
| 4 | `Valid Task` | *(kosong)* | Error: tanggal wajib diisi | Tidak muncul task | ✅ |<img width="300" alt="image" src="https://github.com/user-attachments/assets/d102e2f2-9358-4bfc-9d7c-455108eab31c" />


## 📁 Struktur Folder Gambar
Jika kamu ingin menyimpan bukti gambar secara lokal, gunakan struktur berikut:

