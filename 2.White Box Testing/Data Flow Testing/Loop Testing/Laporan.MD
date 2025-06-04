# White Box Testing - ToDo List App

Dokumentasi ini memfokuskan pada dua metode pengujian **White Box Testing** yang diterapkan pada aplikasi ToDo List berbasis HTML, CSS, dan JavaScript, yaitu **Data Flow Testing** dan **Loop Testing**.

---

## 🔄 Data Flow Testing

### Fokus:

* Titik Definisi (definition): saat variabel diberi nilai
* Titik Penggunaan (use): saat variabel digunakan
* Hindari: data yang disimpan tapi tidak pernah dipakai (dead data)

### Contoh dari `addTodo()`:

| Variabel     | Didefinisikan Di                | Digunakan Di                               |
| ------------ | ------------------------------- | ------------------------------------------ |
| `textTodo`   | `getElementById('title').value` | `generateTodoObject()`                     |
| `timestamp`  | `getElementById('date').value`  | `generateTodoObject()`                     |
| `todoObject` | `generateTodoObject(...)`       | `todos.push()`, lalu dirender dan disimpan |

### Tujuan:

* Pastikan semua input digunakan dengan benar dan efisien
* Hindari penyimpanan nilai yang tidak pernah dimanfaatkan dalam logika program

---

## 🔁 Loop Testing

### Contoh Loop:

```javascript
for (const todoItem of todos) {
  const todoElement = makeTodo(todoItem);
  if (!todoItem.isCompleted)
    uncompletedTODOList.append(todoElement);
  else
    completedTODOList.append(todoElement);
}
```

### Test Case Loop:

| TC | Isi todos\[]               | Expected Output                  |
| -- | -------------------------- | -------------------------------- |
| 1  | Kosong                     | Tidak ada output                 |
| 2  | 1 item belum selesai       | Muncul di "Yang harus dilakukan" |
| 3  | 2 item selesai             | Muncul di "Yang sudah dilakukan" |
| 4  | 1 selesai, 1 belum selesai | Muncul di kedua daftar           |

### Tujuan:

* Memastikan seluruh elemen array `todos` diproses dengan benar oleh perulangan
* Tidak terjadi loop tak terbatas atau kesalahan logika saat iterasi

---
