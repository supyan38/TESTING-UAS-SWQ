# Laporan Desk Checking

**Aplikasi**: Todo List Sederhana  
**Metode Pengujian**: White Box Testing – Desk Checking  
**Tanggal**: 4 Juni 2025  

---

## 1. Tujuan Desk Checking

Desk checking bertujuan untuk memverifikasi dan memvalidasi logika program serta nilai variabel pada proses-proses utama aplikasi todo list, guna memastikan setiap fungsi berjalan sesuai spesifikasi dan tidak terjadi error logika maupun anomali data.

---

## 2. Ruang Lingkup Desk Checking

Desk checking dilakukan pada fungsi-fungsi utama berikut:
- `addTodo()`
- `addTaskToCompleted(todoId)`
- `removeTaskFromCompleted(todoId)`
- `undoTaskFromCompleted(todoId)`
- `saveData()` dan `loadDataFromStorage()`

---

## 3. Prosedur Desk Checking

Desk checking dilakukan dengan cara menelusuri alur eksekusi kode secara manual, mengisi tabel pelacakan variabel, dan memastikan setiap langkah menghasilkan output yang benar. Pemeriksaan dilakukan berdasarkan skenario input yang umum dan ekstrem.

---

## 4. Tabel Desk Checking

### 4.1 Fungsi `addTodo()`

| No. | Langkah Eksekusi            | Variabel Utama | Nilai Awal     | Proses                      | Nilai Akhir         | Output yang Diharapkan         | Status |
|-----|-----------------------------|----------------|----------------|-----------------------------|---------------------|-------------------------------|--------|
| 1   | Ambil input dari form       | textTodo       | -              | Ambil dari input #title     | "Belajar SQA"       | -                             | OK     |
| 2   | Ambil input tanggal         | timestamp      | -              | Ambil dari input #date      | "2025-06-05"        | -                             | OK     |
| 3   | Generate ID unik            | generatedID    | -              | Hasil generateId()          | 1736100000 (misal)  | -                             | OK     |
| 4   | Buat objek todo             | todoObject     | -              | generateTodoObject()        | {id, task, ...}     | -                             | OK     |
| 5   | Tambah ke array todos       | todos          | []             | push(todoObject)            | [todoObject]        | -                             | OK     |
| 6   | Trigger render ulang        | -              | -              | dispatchEvent(RENDER_EVENT) | -                   | Tampilan diperbarui           | OK     |
| 7   | Simpan data ke localStorage | -              | -              | saveData()                  | Data tersimpan      | Data masuk localStorage       | OK     |

**Catatan:**  
Jika input kosong, proses dicegah oleh validasi HTML (`required`). Jika input valid, todo akan muncul di daftar dan tersimpan di localStorage.

---

### 4.2 Fungsi `addTaskToCompleted(todoId)`

| No. | Langkah Eksekusi            | Variabel Utama | Nilai Awal     | Proses                      | Nilai Akhir         | Output yang Diharapkan         | Status |
|-----|-----------------------------|----------------|----------------|-----------------------------|---------------------|-------------------------------|--------|
| 1   | Cari todo berdasarkan ID    | todoId         | ID todo        | findTodo(todoId)            | todo ditemukan      | -                             | OK     |
| 2   | Ubah status menjadi selesai | isCompleted    | false          | todoTarget.isCompleted=true | true                | Todo pindah ke daftar selesai | OK     |
| 3   | Trigger render ulang        | -              | -              | dispatchEvent(RENDER_EVENT) | -                   | Tampilan diperbarui           | OK     |
| 4   | Simpan data ke localStorage | -              | -              | saveData()                  | Data tersimpan      | Data masuk localStorage       | OK     |

---

### 4.3 Fungsi `removeTaskFromCompleted(todoId)`

| No. | Langkah Eksekusi            | Variabel Utama | Nilai Awal     | Proses                      | Nilai Akhir         | Output yang Diharapkan         | Status |
|-----|-----------------------------|----------------|----------------|-----------------------------|---------------------|-------------------------------|--------|
| 1   | Cari index todo berdasarkan ID | todoId       | ID todo        | findTodoIndex(todoId)       | index ditemukan     | -                             | OK     |
| 2   | Hapus todo dari array       | todos          | [todoObject,...]| splice(index, 1)            | todo terhapus       | Todo hilang dari tampilan     | OK     |
| 3   | Trigger render ulang        | -              | -              | dispatchEvent(RENDER_EVENT) | -                   | Tampilan diperbarui           | OK     |
| 4   | Simpan data ke localStorage | -              | -              | saveData()                  | Data tersimpan      | Data masuk localStorage       | OK     |

---

### 4.4 Fungsi `undoTaskFromCompleted(todoId)`

| No. | Langkah Eksekusi            | Variabel Utama | Nilai Awal     | Proses                      | Nilai Akhir         | Output yang Diharapkan         | Status |
|-----|-----------------------------|----------------|----------------|-----------------------------|---------------------|-------------------------------|--------|
| 1   | Cari todo berdasarkan ID    | todoId         | ID todo        | findTodo(todoId)            | todo ditemukan      | -                             | OK     |
| 2   | Ubah status menjadi belum selesai | isCompleted | true          | todoTarget.isCompleted=false| false               | Todo pindah ke daftar belum   | OK     |
| 3   | Trigger render ulang        | -              | -              | dispatchEvent(RENDER_EVENT) | -                   | Tampilan diperbarui           | OK     |
| 4   | Simpan data ke localStorage | -              | -              | saveData()                  | Data tersimpan      | Data masuk localStorage       | OK     |

---

### 4.5 Fungsi `saveData()` dan `loadDataFromStorage()`

| No. | Langkah Eksekusi            | Variabel Utama | Nilai Awal     | Proses                      | Nilai Akhir         | Output yang Diharapkan         | Status |
|-----|-----------------------------|----------------|----------------|-----------------------------|---------------------|-------------------------------|--------|
| 1   | Cek dukungan localStorage   | Storage        | -              | isStorageExist()            | true/false          | Data hanya disimpan jika didukung | OK  |
| 2   | Simpan array todos ke localStorage | todos      | [todoObject,...]| JSON.stringify(todos)      | Data tersimpan      | Data dapat di-load kembali     | OK     |
| 3   | Load data dari localStorage | localStorage   | Data tersimpan | JSON.parse(serializedData)  | todos terisi kembali| Data tampil sesuai sebelum reload| OK   |

---

## 5. Temuan Desk Checking

- Seluruh langkah eksekusi pada fungsi utama berjalan sesuai logika yang diharapkan.
- Tidak ditemukan error logika, anomali variabel, atau output yang tidak sesuai pada setiap proses.
- Validasi input sudah dilakukan pada level HTML (`required`), namun dapat ditingkatkan dengan validasi tambahan pada JavaScript.
- Setiap perubahan data selalu diikuti dengan render ulang tampilan dan penyimpanan data ke localStorage.
- Data konsisten antara array `todos`, tampilan aplikasi, dan data di localStorage.

---

## 6. Kesimpulan

Berdasarkan hasil desk checking, dapat disimpulkan bahwa aplikasi todo list sederhana ini telah memenuhi aspek logika program yang baik, dengan alur data dan proses yang konsisten serta tanpa ditemukan error pada proses utama. Seluruh fungsi berjalan sesuai spesifikasi dan output yang dihasilkan telah sesuai dengan kebutuhan pengguna.

---
