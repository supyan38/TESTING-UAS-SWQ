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
| 1 | Field kosong | Submit | Tidak menambahkan task | Tidak terjadi apa-apa | ✅ | <img width="300" src="https://github.com/user-attachments/assets/c992b96f-3f83-4c11-8a96-8d832f538c04" /> |
| 2 | Field valid | Submit | Task muncul di daftar | Task muncul | ✅ | <img width="300" src="https://github.com/user-attachments/assets/eee38743-f1c2-446a-aedd-6aaf9b9d1fef" /> |
| 3 | Klik centang | - | Task pindah ke selesai | Task pindah | ✅ | <img width="300" src="https://github.com/user-attachments/assets/2583b5d0-ab18-47d6-8958-33f2d6719789" /> |
| 4 | Klik undo | - | Task kembali ke belum selesai | Task kembali | ✅ | <img width="300" src="https://github.com/user-attachments/assets/7aecf097-1ec9-4b68-8276-92ad7897fce5" /> |
