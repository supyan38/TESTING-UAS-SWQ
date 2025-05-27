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
| 1 | Tambah 3 task baru | Refresh browser | Ketiga task tetap muncul | Semua task tampil kembali | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ct-add-refresh.png" /> |
| 2 | Tandai 1 task selesai | Refresh browser | Status selesai tetap muncul (dengan icon/warna berbeda) | Task tetap selesai | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ct-done-refresh.png" /> |
| 3 | Hapus 1 task | Refresh browser | Task tidak muncul lagi | Tidak tampil lagi | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ct-delete-refresh.png" /> |
| 4 | Undo task selesai → jadi belum selesai | Refresh browser | Status kembali ke “belum selesai” | Status tetap | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ct-undo-refresh.png" /> |
| 5 | Tambah task → Tutup browser → Buka kembali | Task tetap muncul | Task tetap tersimpan | ✅ | <img width="300" src="https://github.com/user-attachments/assets/ct-close-open.png" /> |
