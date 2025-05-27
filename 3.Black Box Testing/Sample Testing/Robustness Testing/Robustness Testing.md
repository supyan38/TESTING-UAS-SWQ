# 🧪 Robustness Testing

**Model Black Box Testing** yang bertujuan untuk menguji ketahanan aplikasi terhadap input yang tidak valid atau ekstrem. Tujuannya memastikan aplikasi tetap berjalan dengan baik tanpa error atau crash.

## 🎯 Fitur yang Diuji
- Form Input Task (judul dan tanggal)

## 🧾 Deskripsi
Pengujian ini dilakukan dengan memberikan input yang **tidak sesuai standar**, misalnya teks yang sangat panjang, simbol kompleks, emoji, dan format tanggal yang tidak benar. Fokusnya bukan pada hasil logika aplikasi, tapi pada **ketahanannya terhadap error**.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Jenis Masukan | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-------------|----------------|----------------|------------------|----------------|--------|---------------|
| 1 | 300 karakter huruf `a` | `2025-01-01` | Panjang ekstrem | Aplikasi tetap stabil (boleh gagal simpan) | Tidak crash, input gagal | ✅ | <img width="300" src="https://github.com/user-attachments/assets/7ce964ff-a840-47e6-8d90-f7ef1c669518" /> |
| 2 | `😄🔥💻📚🚀` | `2025-01-01` | Emoji | Aplikasi menerima atau menolak tanpa crash | Task berhasil ditambahkan | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ae56b251-238e-4e7b-ac81-7c7b21d1acd6" /> |
| 3 | `   ` (spasi kosong) | `2025-01-01` | Spasi saja | Aplikasi tetap stabil, task berhasil ditambahkan | Task ditambahkan | ✅ | <img width="300" src="https://github.com/user-attachments/assets/41c01c1c-1e6d-44b5-91df-ea6d325746e7" /> |
| 4 | `\0<script>alert(1)</script>` | `2025-01-01` | Karakter aneh/injeksi | Aplikasi tidak crash / aman | Tidak ada popup/error | ✅ | <img width="300" src="https://github.com/user-attachments/assets/36f5a027-a6ae-490e-9fc6-3c55953b2a5f" /> |

## 📝 Catatan
- Aplikasi stabil pada semua input ekstrem yang diuji.
- Tidak ditemukan error JavaScript atau crash halaman.

