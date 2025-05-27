# 🧪 Sample Testing

**Model Black Box Testing** yang memilih nilai-nilai representatif dari setiap kelas input, untuk memverifikasi bahwa sistem merespons secara konsisten terhadap berbagai sampel data.

## 🎯 Fitur yang Diuji
- Menambahkan Task

## 🧾 Deskripsi
Pengujian ini memilih berbagai jenis input `judul` dan `tanggal` yang mewakili tipe karakter dan panjang yang berbeda, untuk memastikan semua data dapat diproses dengan benar oleh aplikasi.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Jenis Sampel | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|---------------|------------------|----------------|--------|---------------|
| 1 | `Belajar SQA` | `2025-01-01` | Huruf biasa | Task berhasil ditambahkan | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/78e2c984-1053-4e72-ada4-35d008f7dcfb" /> |
| 2 | `123456` | `2025-01-01` | Angka | Task diterima | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/6fe77791-3f32-4f7f-832c-63cb37c8f482" /> |
| 3 | `!@#$%^&*()` | `2025-01-01` | Simbol | Task diterima | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/495ae288-abef-4089-8586-049d7541f713" /> |
| 4 | `Tugas123!` | `2025-01-01` | Kombinasi huruf-angka-simbol | Task berhasil ditambahkan | Muncul di daftar | ✅ | <img width="300" src="https://github.com/user-attachments/assets/f3ee7f6f-e13b-48ce-9a56-119f47675564" /> |


## 📝 Catatan
- Aplikasi menerima input teks dengan berbagai karakter (tanpa filter JS).
- Validasi hanya dilakukan oleh HTML (`required`).
- Tidak ada batas panjang eksplisit, tapi input sangat panjang bisa menyebabkan error tampilan (bergantung browser).
