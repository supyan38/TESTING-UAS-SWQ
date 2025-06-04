## Pattern Testing

Pattern Testing, juga dikenal sebagai "Discovery Testing" atau "Exploratory Testing",
adalah pendekatan pengujian perangkat lunak yang berfokus pada eksplorasi dan
penemuan bug secara kreatif dan inovatif. Teknik ini menekankan pada pemikiran
kritis, intuisi, dan pengalaman tester untuk mengidentifikasi potensi masalah yang
mungkin terlewatkan oleh tes formal.

## 1. Menguji Ferforma Dasar

| No | Langkah Uji          | Deskripsi Aksi             | Harapan                                      | Hasil          | Status  |
| -- | -------------------- | -------------------------- | -------------------------------------------- | -------------- | ------- |
| 1  | Tambah Todo          | Isi form dan klik "Submit" | Todo muncul di daftar "Yang harus dilakukan" | Todo muncul    | ✅ Lulus |
| 2  | Pindahkan ke Selesai | Klik tombol centang        | Todo berpindah ke daftar selesai             | Todo berpindah | ✅ Lulus |
| 3  | Undo dari Selesai    | Klik tombol undo           | Todo kembali ke daftar belum selesai         | Todo kembali   | ✅ Lulus |
| 4  | Hapus Todo           | Klik tombol trash          | Todo dihapus                                 | Todo terhapus  | ✅ Lulus |

## 2. Menguji Batasan dan Skenario Tidak Terduga

| No | Langkah Uji           | Input/Skenario                   | Harapan                  | Hasil                | Status                |
| -- | --------------------- | -------------------------------- | ------------------------ | -------------------- | --------------------- |
| 1  | Kosongkan Input       | Klik "Submit" tanpa mengisi form | Form tidak terkirim      | Tidak terkirim       | ✅ Lulus               |
| 2  | Tanggal Lampau        | Masukkan tanggal kemarin         | Ditolak (idealnya)       | Diterima             | ⚠️ Tidak ada validasi |
| 3  | Karakter Spesial      | Masukkan `!@#$%^&*()` di todo    | Ditampilkan dengan benar | Ditampilkan          | ✅ Lulus               |
| 4  | Tekan Enter di Search | Enter tanpa isi apapun           | Tidak reload halaman     | Halaman tetap        | ✅ Lulus               |
| 5  | Input Sangat Panjang  | Masukkan teks >500 karakter      | UI tetap rapi            | Terpotong namun aman | ✅ Lulus               |

## 3. Menguji Performa dan Stabilitas

| No | Langkah Uji         | Deskripsi                       | Harapan             | Hasil                          | Status       |
| -- | ------------------- | ------------------------------- | ------------------- | ------------------------------ | ------------ |
| 1  | Tambah 100 Todo     | Loop tambah data dummy          | App tetap responsif | App dapat menampilkan 100 todo | ✅ Lulus    |
| 2  | Reload Halaman      | Setelah menambah data           | Data tetap ada      | Muncul dari localStorage       | ✅ Lulus    |
| 3  | Klik cepat berulang | Klik tombol centang/trash cepat | Tidak crash         | Tidak error                    | ✅ Lulus    |

## 4. Menguji Kegunaan dan Pengalaman Pengguna (UX)

| No | Aspek Uji          | Observasi                            | Catatan                       | Status            |
| -- | ------------------ | ------------------------------------ | ----------------------------- | ----------------- |
| 1  | Desain UI          | Simple dan ringan                    | Warna jelas, font terbaca     | ✅ Lulus           |
| 2  | Navigasi           | User mudah pindah antar todo         | Layout jelas                  | ✅ Lulus           |
| 3  | Search             | Langsung menyaring todo saat diketik | Tidak perlu reload            | ✅ Lulus           |
| 4  | Form usability     | Tidak bisa submit kosong             | Sudah ada `required`          | ✅ Lulus           |
| 5  | Placeholder Search | Belum tersedia                       | Perlu ditambah "Cari todo..." | ⚠️ Minor          |
| 6  | Edit Todo          | Tidak ada fitur edit                 | Rekomendasi penambahan        | ⚠️ Belum tersedia |

---

Berdasarkan hasil pengujian menggunakan model Pattern Testing, dapat disimpulkan bahwa aplikasi Todo List telah memenuhi fungsional dasar dengan baik, seperti menambah, menyelesaikan, dan menghapus todo. Aplikasi juga mampu menangani skenario batasan dan input tak terduga, seperti input kosong yang dicegah melalui validasi required. Dari sisi performa, aplikasi tetap responsif saat menambah atau mencari data, bahkan setelah banyak data tersimpan di localStorage. Selain itu, dari sisi kegunaan, penambahan fitur pencarian yang disertai placeholder berhasil meningkatkan pengalaman pengguna dengan memberikan panduan yang jelas dan kemudahan dalam menemukan data todo. Hal ini menunjukkan bahwa aplikasi tidak hanya stabil, tetapi juga ramah terhadap pengguna.
