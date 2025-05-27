# 🧪 Behaviour Testing

Model **Black Box Testing** yang berfokus pada pengujian perilaku aplikasi Todo List.

## 🎯 Fitur yang Diuji
- Form input todo (`judul` dan `tanggal`)
- Penambahan dan pemindahan task

## 🧾 Deskripsi
Mengamati apakah aplikasi merespons dengan benar terhadap input pengguna tanpa melihat struktur kode.

## ✅ Test Case

| No | Aksi Pengguna | Input | Expected Behaviour | Actual Behaviour | Status | Bukti Gambar |
|----|----------------|--------|---------------------|-------------------|--------|---------------|
| 1 | Submit task | `Belajar SWQ`, `2025-05-28` | Task muncul di daftar "Yang harus dilakukan" | Task berhasil ditambahkan | ✅ | poto |
| 2 | Klik centang | - | Task berpindah ke "Yang sudah dilakukan" | Task berhasil dipindah | ✅ | poto |
| 3 | Klik hapus | - | Task hilang dari daftar | Task berhasil dihapus | ✅ | poto |
