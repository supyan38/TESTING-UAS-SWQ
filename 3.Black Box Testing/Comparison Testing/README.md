# 🧪 Comparison Testing

**Model Black Box Testing** yang bertujuan untuk memastikan bahwa sistem menghasilkan hasil yang **sama dan konsisten** dalam dua kondisi berbeda, misalnya sebelum dan sesudah reload, atau di dua browser berbeda.

## 🎯 Fitur yang Diuji
- Menambahkan Task
- Menandai Task Selesai
- Menghapus Task
- Melakukan Undo
- Reload halaman

## 🧾 Deskripsi
Testing dilakukan dengan **membandingkan kondisi sebelum dan sesudah browser direfresh** untuk memastikan:
- Data tersimpan di `localStorage`
- Status task tetap sesuai terakhir kali
- Tidak ada kehilangan data

## ✅ Test Case

| No | Aksi Awal | Tindakan Pembanding | Expected Result | Actual Result | Status | Bukti Gambar |
|----|-----------|----------------------|------------------|----------------|--------|---------------|
| 1 | Tambah 3 task baru | Refresh browser | Ketiga task tetap muncul | Semua task tampil kembali | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ffbc02d6-f0e3-4452-b34e-25b7a75899fe" /> |
| 2 | Tandai 1 task selesai | Refresh browser | Status selesai tetap muncul (dengan icon/warna berbeda) | Task tetap selesai | ✅ | <img width="300" src="https://github.com/user-attachments/assets/5fc1d5e9-2104-460b-a71e-116eedd83d74" /> |
| 3 | Hapus 1 task | Refresh browser | Task tidak muncul lagi | Tidak tampil lagi | ✅ | <img width="300" src="https://github.com/user-attachments/assets/6ce87bab-5967-486b-b27c-4d9ba2286b37" /> |
| 4 | Undo task selesai → jadi belum selesai | Refresh browser | Status kembali ke “belum selesai” | Status tetap | ✅ | <img width="300" src="https://github.com/user-attachments/assets/21690618-f166-408b-b8c3-e2c4fc02f32e" /> <img width="300" src="https://github.com/user-attachments/assets/06cb2854-f45b-45a8-a7a3-cf8de22d2a13" /> |
| 5 | Tambah task → Tutup browser → Buka kembali | Task tetap muncul | Task tetap tersimpan | ✅ |<img width="300" alt="image" src="https://github.com/user-attachments/assets/fdb72cd0-9774-4d36-8a8d-64c5addafbae" />
