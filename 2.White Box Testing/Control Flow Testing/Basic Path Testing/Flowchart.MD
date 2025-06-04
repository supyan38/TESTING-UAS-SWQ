# ✅ White Box Testing - Fungsi `addTodo()` (ToDo List App)

## 🎯 Tujuan
Melakukan **Control Flow Testing** dan **Basic Path Testing** pada fungsi `addTodo()` di aplikasi ToDo List berbasis HTML, CSS, dan JavaScript.

---

## 🔁 Control Flow Testing

### Deskripsi Alur Logika:

1. Ambil nilai dari input `title` dan `date`
2. (Jika ada validasi) Periksa apakah input kosong
3. Generate ID menggunakan timestamp
4. Buat object `todo`
5. Masukkan ke array `todos`
6. Trigger event `render-todo`
7. Simpan ke `localStorage`

### Elemen Kontrol yang Diuji:
- `if` untuk validasi input
- Proses sequential (buat ID → buat object → push ke array)
- Fungsi eksternal: `dispatchEvent`, `saveData()`

---

## 📉 Flowchart

![Flowchart addTodo](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAdQAAAH0CAYAAADfmcUeAAAgAElEQVR4nOzdeXgcx5nv/eeJEF...TRUNCATED...)

> 📝 *Gambar flowchart sudah ditempel langsung secara base64.*

---

## 🧮 Basic Path Testing

### Cyclomatic Complexity
Menggunakan rumus:  
`V(G) = E - N + 2`  
- E (Edge): 6  
- N (Node): 5  
- V(G) = 6 - 5 + 2 = **3**

Artinya: terdapat **3 jalur dasar (basic paths)** yang perlu diuji.

### Test Case:

| TC | Input Title     | Input Date     | Expected Result                                 |
|----|------------------|----------------|--------------------------------------------------|
| 1  | `""`             | `2025-06-01`   | Alert: "Form tidak boleh kosong!"              |
| 2  | `"Belajar JS"`   | `""`           | Alert: "Form tidak boleh kosong!"              |
| 3  | `"Belajar JS"`   | `2025-06-01`   | ToDo tersimpan, dirender, dan masuk ke storage  |

---

## 🧠 Kesimpulan

- Control Flow Testing membantu mengecek apakah semua **alur logika** kode sudah diuji
- Basic Path Testing memastikan semua **jalur minimum logika** diuji secara efisien
- Dengan pengujian ini, kita bisa meningkatkan keandalan fungsi `addTodo()`

---
