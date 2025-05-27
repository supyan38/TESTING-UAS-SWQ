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
| 1 | Belum Selesai | Hapus | Task hilang dari daftar aktif | Task berhasil dihapus | ✅ |<img width="959" alt="image" src="https://github.com/user-attachments/assets/b13d8913-789f-4ce6-a660-06482fb5c79c" /> | <img width="959" alt="image" src="https://github.com/user-attachments/assets/25cda08b-41f9-4ec7-9ed6-4c1805e30ea2" />

| 2 | Selesai | Hapus | Task hilang dari daftar selesai | Task berhasil dihapus | ✅ |<img width="958" alt="image" src="https://github.com/user-attachments/assets/aa9c56f2-5306-4c90-b88c-aa55e2b9b66e" /> |<img width="956" alt="image" src="https://github.com/user-attachments/assets/824c525c-7830-4258-b9b0-fbf58c5be33e" /> | <img width="959" alt="image" src="https://github.com/user-attachments/assets/abf05b76-298e-446f-a084-48e0f82af3ef" />

| 3 | Selesai | Undo | Task pindah ke daftar aktif | Task dipindahkan | ✅ |<img width="959" alt="image" src="https://github.com/user-attachments/assets/fd787aa2-2914-4fe7-bf2b-0f7ec6855025" /> |<img width="959" alt="image" src="https://github.com/user-attachments/assets/4feb7a90-9fb5-4d66-aef3-200f745da4dd" /> |<img width="959" alt="image" src="https://github.com/user-attachments/assets/46dff713-88f0-4f7d-8063-85d0d8d8009d" />

| 4 | Belum Selesai | Undo | Tidak terjadi apa-apa | Tidak ada perubahan | ✅ |<img width="959" alt="image" src="https://github.com/user-attachments/assets/c2810490-a8f1-4d99-9489-e90e3e07b489" />


## 📝 Catatan
- Aplikasi mengubah status dan daftar task berdasarkan aksi pengguna tanpa konfirmasi tambahan.
- Undo hanya berlaku jika task sudah diselesaikan.
- Hapus berfungsi di kedua status, tetapi task langsung hilang.
