# 🧪 Behaviour Testing

Model **Black Box Testing** yang berfokus pada pengujian perilaku aplikasi Todo List.

## 🎯 Fitur yang Diuji
- Form input todo (`judul` dan `tanggal`)
- Penambahan dan pemindahan task

## 🧾 Deskripsi
Mengamati apakah aplikasi merespons dengan benar terhadap input pengguna tanpa melihat struktur kode.

## ✅ Test Case

| No | Aksi Pengguna  | Input                     | Expected Behaviour                                | Actual Behaviour           | Status | Bukti Gambar |
|----|----------------|---------------------------|----------------------------------------------------|-----------------------------|--------|---------------|
| 1  | Submit task    | `Belajar SWQ`, `2025-05-28` | Task muncul di daftar "Yang harus dilakukan"      | Task berhasil ditambahkan  | ✅     | ![Gambar 1](https://github.com/user-attachments/assets/72ca8562-e996-4fb7-b272-fa0a52cf7c50) |
| 2  | Klik centang   | -                         | Task berpindah ke "Yang sudah dilakukan"           | Task berhasil dipindah     | ✅     | ![Gambar 2](https://github.com/user-attachments/assets/7ebe0b88-e1ee-4cc5-8097-f89f68f83005) |
| 3  | Klik hapus     | -                         | Task hilang dari daftar                            | Task berhasil dihapus      | ✅     | ![Gambar 3](https://github.com/user-attachments/assets/d99632fb-6c45-480d-86d5-c7d805486d63) |

<!-- Untuk memperbesar gambar di luar tabel, tambahkan kode di bawah ini jika markdown viewer mendukung HTML -->

<br/>

### 🖼️ Bukti Gambar Ukuran Besar

#### ✅ Submit Task
<img src="https://github.com/user-attachments/assets/72ca8562-e996-4fb7-b272-fa0a52cf7c50" width="1300" />

#### ✅ Klik Centang
<img src="https://github.com/user-attachments/assets/7ebe0b88-e1ee-4cc5-8097-f89f68f83005" width="1300" />

#### ✅ Klik Hapus
<img src="https://github.com/user-attachments/assets/d99632fb-6c45-480d-86d5-c7d805486d63" width="1300" />
