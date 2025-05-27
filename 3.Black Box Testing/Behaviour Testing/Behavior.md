# 🧪 Boundary Value Analysis (BVA)

**Model Pengujian Black Box** yang menguji nilai input pada batas minimal dan maksimal untuk memastikan sistem dapat menangani nilai ekstrem dengan benar.

## 🎯 Fitur yang Diuji
- Menambahkan Task Baru (Form Input)

## 🧾 Deskripsi
Dilakukan pengujian terhadap batas input `judul` dan `tanggal` pada form tambah task. Tujuan pengujian ini untuk memastikan sistem memvalidasi nilai minimum, maksimum, dan nilai kosong.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|------------------|----------------|--------|---------------|
| 1 | `A` (1 karakter) | `2025-01-01` | Task berhasil ditambah | Task muncul di daftar | ✅ |<img width="959" alt="image" src="https://github.com/user-attachments/assets/49c603b6-2aae-41f9-a50c-30f80ed038f6" />
 |
| 2 | *(kosong)* | `2025-01-01` | Error: judul tidak boleh kosong | Task tidak ditambah | ✅ | ![TC2](./img/tc2-judul-kosong.png) |
| 3 | `A...A` (256 karakter) | `2025-01-01` | Error: input terlalu panjang | Tidak diproses | ✅ | ![TC3](./img/tc3-panjang.png) |
| 4 | `Valid Task` | *(kosong)* | Error: tanggal wajib diisi | Tidak muncul task | ✅ | ![TC4](./img/tc4-tanggal-kosong.png) |
| 5 | `Valid Task` | `invalid-date` | Error: format tanggal salah | Tidak diproses | ✅ | ![TC5](./img/tc5-tanggal-invalid.png) |

## 📁 Struktur Folder Gambar
Letakkan semua gambar di dalam folder `img/` di dalam direktori ini, contoh:
 
