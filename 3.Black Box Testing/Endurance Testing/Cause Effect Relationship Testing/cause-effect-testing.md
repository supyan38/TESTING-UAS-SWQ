# 🔍 Cause-Effect Relationship Testing

Model **Black Box Testing** yang menganalisis hubungan sebab-akibat dari aksi pengguna terhadap respons sistem.

## 🎯 Fitur yang Diuji
- Validasi input
- Respon UI terhadap aksi

## 🧾 Deskripsi
Pengujian difokuskan pada logika hubungan antara input pengguna dan reaksi sistem yang terjadi.

## ✅ Test Case

| No | Kondisi | Aksi | Expected Effect | Actual Result | Status | Bukti Gambar |
|----|---------|------|------------------|----------------|--------|---------------|
| 1 | Field kosong | Submit | Tidak menambahkan task | Tidak terjadi apa-apa | ✅ | ![img](https://via.placeholder.com/300x100?text=Cause+1) |
| 2 | Field valid | Submit | Task muncul di daftar | Task muncul | ✅ | ![img](https://via.placeholder.com/300x100?text=Cause+2) |
| 3 | Klik centang | - | Task pindah ke selesai | Task pindah | ✅ | ![img](https://via.placeholder.com/300x100?text=Cause+3) |
| 4 | Klik undo | - | Task kembali ke belum selesai | Task kembali | ✅ | ![img](https://via.placeholder.com/300x100?text=Cause+4) |
