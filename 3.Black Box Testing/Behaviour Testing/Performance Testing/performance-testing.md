# 🚀 Performance Testing

Model **Black Box Testing** yang bertujuan untuk mengukur waktu respon aplikasi saat melakukan aksi penting.

## 🎯 Fitur yang Diuji
- Loading halaman
- Submit, update, dan hapus task

## 🧾 Deskripsi
Pengujian dilakukan dengan memanfaatkan Chrome DevTools untuk mengukur waktu eksekusi aktivitas pengguna.

## 🔍 Hasil Uji

| Kegiatan | Waktu Respon (Chrome DevTools) | Status |
|----------|-------------------------------|--------|
| Load halaman pertama kali | ±150ms | ✅ |
| Submit task | ±50ms | ✅ |
| Pindah task (centang) | ±30ms | ✅ |
| Hapus task | ±40ms | ✅ |

## 🔎 Hasil Uji PageSpeed Insight
<img width="600" src="https://github.com/user-attachments/assets/9b983cec-f039-4e20-a1dc-41084d2ec796" />


**Tools:** 
- Chrome DevTools > Network & Performance tab
- PageSpeed Insight


