**📘 Definisi :**
Code Walkthrough adalah **review kode secara informal maupun formal**, yang dilakukan oleh developer bersama tim untuk:

* Memahami logika kode
* Mengidentifikasi potensi error
* Meningkatkan kualitas program


### ✅ Tujuan Code Walkthrough

* Bukan untuk "mengevaluasi hasil akhir" seperti pengujian fungsional
* Tapi untuk **meninjau dan berdiskusi langsung logika program**


---

### 📌 Contoh Code Walkthrough dari Fungsi `addTodo()`


🧠 **Fungsi**:

```javascript
function addTodo() {
    const textTodo = document.getElementById('title').value;
    const timestamp = document.getElementById('date').value;

    const generatedID = generateId();
    const todoObject = generateTodoObject(generatedID, textTodo, timestamp, false);
    todos.push(todoObject);

    document.dispatchEvent(new Event(RENDER_EVENT));
    saveData();
}
```

---

### 👣 Langkah-langkah Walkthrough:

| Baris | Penjelasan                                                               |
| ----- | ------------------------------------------------------------------------ |
| 2     | Ambil nilai dari input "title"                                           |
| 3     | Ambil nilai dari input "date"                                            |
| 5     | Buat ID unik menggunakan waktu saat ini                                  |
| 6     | Buat object todo berisi data (id, task, tanggal, status selesai = false) |
| 7     | Masukkan object ini ke dalam array `todos`                               |
| 9     | Trigger event untuk render ulang tampilan todo list                      |
| 10    | Panggil fungsi `saveData()` untuk menyimpan ke localStorage              |

---

### 💥 Potensi Masalah yang Ditemukan Saat Walkthrough:

* **Belum ada validasi** untuk input kosong (🛠 disarankan ditambahkan)
* **Tanpa batas maksimal input** (misal user isi 1000 todo)
* **ID berdasarkan waktu** → bisa bentrok jika sangat cepat diisi (kemungkinan kecil)

---

### ✅ Perbaikan yang Diusulkan Saat Walkthrough:

```javascript
if (textTodo.trim() === "" || timestamp.trim() === "") {
  alert("Title dan tanggal tidak boleh kosong!");
  return;
}
```

---

### 📋 Hasil Walkthrough:

| Aspek            | Status      | Catatan                                     |
| ---------------- | ----------- | ------------------------------------------- |
| Input validation | ❌ Belum ada | Perlu dicegah agar user tidak submit kosong |
| Struktur kode    | ✅ Rapi      | Mudah dibaca dan diikuti                    |
| Penyimpanan data | ✅ Sudah ada | Disimpan ke localStorage                    |
| Potensi bug ID   | ⚠️ Kecil    | Bisa dicegah dengan ID + random tambahan    |

---
