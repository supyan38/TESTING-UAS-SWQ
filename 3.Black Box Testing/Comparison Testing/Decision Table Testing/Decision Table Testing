# 🧪 Decision Table Testing

**Model Black Box Testing** yang menggunakan tabel keputusan untuk menguji kombinasi logika kondisi dan aksi, agar sistem merespons dengan benar sesuai keputusan yang berlaku.

## 🎯 Fitur yang Diuji
- Menghapus Task
- Undo Task

## 🧾 Deskripsi
Pengujian ini mengevaluasi kombinasi **status task (selesai atau belum selesai)** dan aksi pengguna **(hapus atau undo)**. Tujuannya untuk memastikan bahwa setiap kombinasi menghasilkan perilaku sistem yang tepat.

## 📊 Decision Table

| No | Kondisi: Status Task | Aksi | Expected Result | Actual Result | Status | Bukti Gambar |
|----|----------------------|------|------------------|----------------|--------|---------------|
| 1 | Belum Selesai | Hapus | Task hilang dari daftar aktif | Task berhasil dihapus | ✅ | <img width="300" src="https://github.com/user-attachments/assets/dt-hapus-belumselesai.png" /> |
| 2 | Selesai | Hapus | Task hilang dari daftar selesai | Task berhasil dihapus | ✅ | <img width="300" src="https://github.com/user-attachments/assets/dt-hapus-selesai.png" /> |
| 3 | Selesai | Undo | Task pindah ke daftar aktif | Task dipindahkan | ✅ | <img width="300" src="https://github.com/user-attachments/assets/dt-undo-selesai.png" /> |
| 4 | Belum Selesai | Undo | Tidak terjadi apa-apa | Tidak ada perubahan | ✅ | <img width="300" src="https://github.com/user-attachments/assets/dt-undo-belumselesai.png" /> |

## 📁 Struktur Folder Gambar

