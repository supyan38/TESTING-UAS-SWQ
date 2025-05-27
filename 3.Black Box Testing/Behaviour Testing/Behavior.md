# 🧪 Boundary Value Analysis (BVA)

**Model Pengujian Black Box** yang menguji nilai input pada batas minimal dan maksimal untuk memastikan sistem dapat menangani nilai ekstrem dengan benar.

## 🎯 Fitur yang Diuji
- Menambahkan Task Baru

## 🧾 Deskripsi
Dilakukan pengujian terhadap batas input `judul` dan `tanggal` saat menambahkan task baru.

## ✅ Test Case

| No | Input Judul | Input Tanggal | Expected Result | Actual Result | Status |
|----|-------------|----------------|------------------|----------------|--------|
| 1 | `A` (1 karakter) | `2025-01-01` | Task berhasil ditambah | Task muncul di daftar | ✅ |
| 2 | *(kosong)* | `2025-01-01` | Error: judul tidak boleh kosong | Task tidak ditambah | ✅ |
| 3 | `A...A` (256 karakter) | `2025-01-01` | Error: input terlalu panjang | Ditolak oleh sistem | ✅ |
| 4 | `Valid Task` | *(kosong)* | Error: tanggal wajib diisi | Tidak muncul task | ✅ |
| 5 | `Valid Task` | `invalid-date` | Error: format tanggal salah | Tidak diproses | ✅ |

## 📝 Catatan
- Uji dilakukan di `form` input utama.
- Sistem tidak menunjukkan alert khusus tapi tidak memproses input invalid.
