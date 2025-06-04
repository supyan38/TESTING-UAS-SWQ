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
|validasi Form            |
|-------------------------|
|Tambah Todo List         |
|-------------------------|
|Tandai Todo List Selesai |
|-------------------------|
|Undo Todo List           |
|-------------------------|
|Hapus Todo List          |
|-------------------------|
|Simpan Local Storange    |
|-------------------------|
|Tampilkan Todo List      |
|-------------------------|
