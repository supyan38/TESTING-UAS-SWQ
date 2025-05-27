# 🧪 Equivalence Partitioning (EP)

**Model Pengujian Black Box** yang membagi data masukan (input) ke dalam kelas-kelas yang setara (ekivalen), sehingga hanya perlu menguji satu atau dua nilai per kelas untuk mewakili keseluruhan.

## 🎯 Fitur yang Diuji
- Menambahkan Task Baru melalui form input

## 🧾 Deskripsi
Pengujian ini bertujuan memastikan bahwa input `judul` dan `tanggal` diperlakukan secara konsisten dalam kelas data:
- Kelas Valid → harus diterima
- Kelas Tidak Valid → harus ditolak (melalui validasi HTML)

## ✅ Test Case

| No | Input Judul | Input Tanggal | Kelas | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|--------|------------------|----------------|--------|---------------|
| 1 | `Belajar SQA` | `2025-01-01` | Valid | Task berhasil ditambahkan | Task muncul di daftar | ✅ | <img width="960" alt="image" src="https://github.com/user-attachments/assets/36d95fa7-5600-4a58-a98a-bd4a66189c89" />
| 2 | *(kosong)* | `2025-01-01` | Tidak Valid (judul kosong) | Ditolak oleh HTML form | Tidak ditambahkan | ✅ |<img width="960" alt="image" src="https://github.com/user-attachments/assets/040dcf2c-699c-41d4-a9aa-2f14d113f297" />

| 3 | `!!!@#` | `2025-01-01` | Valid (judul simbol) | Task diterima | Task muncul di daftar | ✅ |<img width="960" alt="image" src="https://github.com/user-attachments/assets/0c89e40c-52bb-4750-bc7f-fedea86a4d9c" />

| 4 | `Tugas` | *(kosong)* | Tidak Valid (tanggal kosong) | Ditolak oleh HTML form | Tidak ditambahkan | ✅ | <img width="960" alt="image" src="https://github.com/user-attachments/assets/e8654e24-5f2c-45d1-8cf4-cbbd067813b6" />
|

