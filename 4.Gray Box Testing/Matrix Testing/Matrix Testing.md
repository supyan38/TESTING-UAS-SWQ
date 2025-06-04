# Matrix Testing

Matrix Testing merupakan teknik pengujian perangkat lunak yang sistematis dan terstruktur untuk
menguji berbagai kombinasi input dan kondisi dalam suatu aplikasi. Teknik ini membantu
mengidentifikasi bug yang disebabkan oleh interaksi antara parameter atau faktor yang berbeda
dalam aplikasi.
Langkah Skenario Matrix Testing :
“Misalkan aplikasi buku memiliki fitur pencarian yang memungkinkan pengguna mencari buku
berdasarkan judul, penulis, dan tahun terbit.”
1. Definisikan Parameter dan Kondisi
2. Membuiat Tabel Matriks
3. Menjalankan Test Case
4. Analisis Hasil

---

## 1. Definisi Parameter dan Kondisi

Parameter (Faktor yang Diuji):
Input Teks Todo (InputText)

- Input Tanggal (InputDate)

- Tombol Tambah Todo (SubmitButton)

- Tombol Tandai Selesai (CheckButton)

- Tombol Undo (UndoButton)

- Tombol Hapus (TrashButton)

- LocalStorage (StorageStatus)

Kondisi yang Diuji:
Input valid atau tidak

- Tombol ditekan atau tidak

- Data tersimpan atau tidak

- Todo berpindah status atau tidak

- Todo tampil atau tidak di DOM

## 2. Tabel Matriks

| Fitur                   | Input Text  | Input Tanggal | Submit Button | Check Button | Undo Button | Trash Button | Storange Status |
|-------------------------|-------------|---------------|---------------|--------------|-------------|--------------|-----------------|
|validasi Form            | ✅          | ✅           | ✅            |              |             |              |                 |
|Tambah Todo List         | ✅          | ✅           | ✅            |              |             |              |                 |
|Tandai Todo List Selesai |             |               |                | ✅          |             |              | ✅              |
|Undo Todo List           |             |               |                |              | ✅         |              | ✅              |
|Hapus Todo List          |             |               |                |              |             | ✅          | ✅              |
|Simpan Local Storange    | ✅          | ✅           | ✅            | ✅           | ✅          | ✅          | ✅              |
|Tampilkan Todo List      |             |               |                |              |              |             | ✅              |

Pada bagian yang ditandai cehecklist, ditandai bahwa bagian tersebut mempengaruhi proses yang terjadi pada setiap fitur.

## 3. Implementasi Test Case

| No  | Skenario                           | Input                  | Aksi               | Ekspektasi                                                         |
| --- | ---------------------------------- | ---------------------- | ------------------ | ------------------------------------------------------------------ |
| TC1 | Isi todo + tanggal → klik submit   | "Membaca", 2025-06-02  | Klik tombol tambah | Todo tampil di daftar aktif dan tersimpan ke localStorage          |
| TC2 | Kosongkan input teks → klik submit | "", 2025-06-01         | Klik tombol tambah | Validasi muncul, todo tidak ditambahkan                            |
| TC3 | Tandai todo sebagai selesai        | Todo aktif ada         | Klik ikon centang  | Todo berpindah ke daftar selesai dan statusnya `isCompleted: true` |
| TC4 | Undo todo selesai                  | Todo di daftar selesai | Klik ikon undo     | Todo kembali ke daftar aktif (`isCompleted: false`)                |
| TC5 | Hapus todo dari daftar selesai     | Todo di daftar selesai | Klik ikon trash    | Todo dihapus dari array dan hilang dari DOM                        |
| TC6 | Refresh halaman                    | Data ada di storage    | Muat ulang browser | Semua todo muncul kembali sesuai status                            |

## 4. Analisa Hasil Pada Test

| Test Case | Status | Keterangan                                                               |
| --------- | ------ | -------------------------------------------------------------------------|
| TC1       | ✅      | Fitur tambah todo bekerja, data tersimpan dan ditampilkan               |
| TC2       | ✅      | Validasi input kosong muncul, tidak terjadi penambahan                  |
| TC3       | ✅      | Status `isCompleted` berubah, todo berpindah ke daftar selesai          |
| TC4       | ✅      | Status kembali ke aktif, todo muncul di daftar aktif                    |
| TC5       | ✅      | Todo berhasil dihapus dan tidak muncul di daftar maupun array           |
| TC6       | ✅      | LocalStorage menyimpan dan memuat data dengan benar saat reload halaman |

---

Berdasarkan pengujian menggunakan metode Matrix Testing, seluruh fungsi utama aplikasi TodoList berjalan dengan baik dan saling terhubung antar parameter seperti input teks, tanggal, tombol aksi, serta penyimpanan data di localStorage. Setiap test case yang dijalankan, termasuk penambahan, penyelesaian, pengembalian, penghapusan, dan pemuatan ulang data, menunjukkan hasil sesuai ekspektasi tanpa adanya error atau kegagalan proses. Hal ini membuktikan bahwa integrasi antar komponen aplikasi berfungsi secara konsisten dan layak untuk digunakan dalam skenario penggunaan nyata.
