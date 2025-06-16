# MCGoGo Enemy Predictor oleh 

**MCGoGo Enemy Predictor** adalah aplikasi yang dibangun menggunakan Next.js, dirancang khusus untuk membantu pemain dalam memprediksi musuh di game Magic Chess. Aplikasi ini memanfaatkan logika prediksi yang memerlukan beberapa input manual dari pengguna, seperti nama p8 dan input untuk ronde 2, 4, 5, dan 6, sehingga memungkinkan prediksi otomatis untuk beberapa ronde.

**Fitur Utama:**

- **Tabel Ronde 1–7:**  
  Tempat di mana pengguna dapat mengisi data dan mendapatkan prediksi secara otomatis.

- **Tabel Ronde 8–14:**  
  Merupakan salinan dari tabel ronde 1–7 dengan nomor ronde yang di-offset (contoh: 8 = ronde 1, 9 = ronde 2, dan seterusnya). Tabel ini bersifat read-only dan dapat ditampilkan atau disembunyikan menggunakan tombol toggle.

## Preview

Lihat Preview aplikasi di: [https://prediksi-musuh-mcgg.vercel.app/](https://prediksi-musuh-mcgg.vercel.app/)

## Cara Kerja

- **Input Global:**  
  Masukkan nama **p8** (musuh pertama/mantan pertama) yang akan digunakan di ronde 1.

- **Tabel Ronde 1–7:**  
  - **Ronde 1:** Diisi otomatis dengan *User  vs = p8* dan *p8 vs = "user"*.
  - **Ronde 2 & 4:** Diisi secara manual oleh pengguna.
  - **Ronde 3:** Terprediksi berdasarkan ronde 2 (User  vs = input p8 vs ronde 2, dan sebaliknya).
  - **Ronde 5:** User vs terprediksi dari input p8 vs di ronde 4, sedangkan p8 vs harus diisi manual (dengan placeholder dinamis).
  - **Ronde 6:** User vs terprediksi dari input p8 vs di ronde 5, sedangkan p8 vs harus diisi manual (misalnya: p6).
  - **Ronde 7:** Terprediksi otomatis berdasarkan ronde 6.

- **Tabel Ronde 8–14:**  
  Merupakan duplikasi dari tabel ronde 1–7 dengan nomor ronde ditambahkan 7. Tabel ini hanya untuk tampilan (read-only).

## Cara Menjalankan

Pastikan Anda telah menginstal [Node.js](https://nodejs.org/) (versi 16) dan ikuti langkah-langkah berikut:

1. Clone repository ini:
   ```bash
   git clone https://github.com/username/mcgogo-enemy-predictor.git
   ```
