
# ✅ Behaviour Testing – Todo List App

Dokumen ini menjelaskan **Behaviour Testing** untuk aplikasi Todo List berbasis web.

## 📋 Tujuan

Memastikan bahwa setiap **perilaku pengguna terhadap aplikasi** menghasilkan **output yang sesuai** dengan yang diharapkan, tanpa melihat kode internal (black box).

---

## 🧠 Daftar Behaviour dan Expected Output

### 1. Menambahkan Task
- **Behaviour**: User mengisi input dan klik tombol `Add` atau tekan `Enter`
- **Expected Result**: Task baru muncul di daftar

### 2. Menambahkan Task Kosong
- **Behaviour**: User klik tombol `Add` tanpa mengisi input
- **Expected Result**: Tidak ada task ditambahkan, validasi ditampilkan (jika ada)

### 3. Menandai Task Selesai
- **Behaviour**: User klik ikon checklist pada task
- **Expected Result**: Task diberi tanda selesai (misalnya berubah warna atau dicoret)

### 4. Menghapus Task
- **Behaviour**: User klik ikon trash pada task
- **Expected Result**: Task dihapus dari daftar

### 5. Undo Penghapusan Task
- **Behaviour**: User klik tombol `Undo` setelah menghapus task
- **Expected Result**: Task terakhir yang dihapus dikembalikan ke daftar

### 6. Reload Halaman
- **Behaviour**: User menekan `F5` atau reload browser
- **Expected Result**: Semua task tetap ada (jika menggunakan `localStorage`)

### 7. Input Task dengan Karakter Khusus
- **Behaviour**: User masukkan karakter seperti `@#$%` lalu klik Add
- **Expected Result**: Task ditambahkan tanpa error

---

## 🧪 Behaviour Testing Table

| Test Case              | User Action              | Expected Behaviour         | Status |
|------------------------|--------------------------|----------------------------|--------|
| Add valid task         | "Belajar JS" → Add       | Task muncul                | ✅     |
| Add empty task         | "" → Add                 | Task tidak ditambahkan     | ✅     |
| Complete task          | Klik checklist           | Task dicoret/sesuai style  | ✅     |
| Delete task            | Klik ikon trash          | Task hilang                | ✅     |
| Undo delete            | Klik Undo                | Task kembali               | ✅     |
| Reload browser         | F5                       | Task tetap ada             | ✅     |
| Add special characters | "@task!" → Add           | Task muncul                | ✅     |

---

## 📦 Catatan

- Penyimpanan data menggunakan **localStorage**, sehingga task tetap ada meski halaman di-reload.
- Semua behaviour diuji secara manual melalui **User Interface** (UI) aplikasi.
