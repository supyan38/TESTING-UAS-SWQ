# 🧪 Sample Testing

**Model Black Box Testing** yang memilih nilai-nilai representatif dari setiap kelas input, untuk memverifikasi bahwa sistem merespons secara konsisten terhadap berbagai sampel data.

## 🎯 Fitur yang Diuji
- Menambahkan Task

## 🧾 Deskripsi
Pengujian ini memilih berbagai jenis input `judul` dan `tanggal` yang mewakili tipe karakter dan panjang yang berbeda, untuk memastikan semua data dapat diproses dengan benar oleh aplikasi.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Jenis Sampel | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|---------------|------------------|----------------|--------|---------------|
| 1 | `Belajar SQA` | `2025-01-01` | Huruf biasa | Task berhasil ditambahkan | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/st-huruf.png" /> |
| 2 | `123456` | `2025-01-01` | Angka | Task diterima | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/st-angka.png" /> |
| 3 | `!@#$%^&*()` | `2025-01-01` | Simbol | Task diterima | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/st-simbol.png" /> |
| 4 | `Tugas123!` | `2025-01-01` | Kombinasi huruf-angka-simbol | Task berhasil ditambahkan | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/st-kombinasi.png" /> |
| 5 | `aaaaaaaa...` (256 karakter) | `2025-01-01` | Panjang ekstrem | Task gagal atau dibatasi | Tidak muncul / ditolak | ✅ | <img width="300" src="https://github.com/user-attachments/assets/st-panjang.png" /> |

## 📁 Struktur Folder Gambar

