Pengujian Array Ortogonal (OAT) adalah teknik pengujian perangkat lunak yang
menggunakan array ortogonal untuk membuat kasus uji. Ini adalah pendekatan
pengujian statistik yang sangat berguna ketika sistem yang akan diuji memiliki input
data yang besar. Pengujian susunan ortogonal membantu memaksimalkan cakupan
pengujian dengan memasangkan dan menggabungkan input serta menguji sistem dengan
jumlah kasus pengujian yang relatif lebih sedikit untuk menghemat waktu
---
Pada pengujian ini menggunakan software Tode list, yaitu software yang digunakan untuk membuat daftar list kegiatan yang harus dilakukan dalam jangka waktu tertentu. Pada software ini  terdapat dua input yaitu judul (Masukan Hal yang harus dilakukan) dan Tanggal (Masukan tanggal harus selesai). Kemudian ketika data input di submit data akan tersimpan ke memori tanpa menggunakan database. 
Dalam pengujian ini alikasi Todo List dibagi menjadi beberapa tahap pengujian untuk uji Orthogonal Array Testing yaitu , sebagai berikut :
---
##1.	Faktor dan Level yang diuji
Pada tahap ini terdapat dua faktor sesui input yang digunakan yaitu Judul  tugas dan Tanggal Deadline, kemudian dibagi menjadi 3 level untuk dilakukan uji:

| Faktor          | Level 1            | Level 2                                   | Level 3    |
|-----------------|--------------------|-------------------------------------------|------------|
| Judul Tugas     | Pendek "Membaca"   | Panjang "Membaca Buku Sejarah Penjejehan" | Kosong     |
| Tanggal Deadline| Tanggal Hari ini   | Waktu mendatang                           | Kosong     |

