# Pertemuan 10 - Local Storage Menggunakan SharedPreferences

Repositori ini dibuat untuk memenuhi tugas Praktikum Pemrograman Mobile - Modul 10 mengenai implementasi penyimpanan data lokal (*local storage*) pada aplikasi Flutter menggunakan *package* `shared_preferences`.

## 📌 Pembahasan Singkat Praktikum

Pada praktikum Modul 10 ini, fokus utama materi adalah memahami dan mengimplementasikan **Local Storage** pada perangkat mobile. 

* **Konsep Dasar:** Penyimpanan data dilakukan secara lokal di dalam memori internal perangkat pengguna tanpa bergantung pada koneksi internet. Metode ini sangat berguna untuk menjaga persistensi data ringan seperti status sesi login pengguna (*session*), preferensi tema aplikasi (*dark/light mode*), maupun pengaturan (*settings*) aplikasi.
* **SharedPreferences:** Praktikum ini memanfaatkan *package* `shared_preferences` untuk menyimpan data sederhana berbasis pasangan kunci-nilai (*key-value pair*). Tipe data yang didukung oleh package ini terbatas pada tipe primitif seperti `String`, `int`, `double`, `boolean`, dan `List<String>`.
* **Fitur yang Diimplementasikan:** Membuat alur autentikasi sederhana (Login, Auto-Login pasca aplikasi ditutup, dan Logout) dengan menyimpan *key* `isLogin` (bool) dan `username` (String) ke dalam penyimpanan lokal perangkat.

---

## 🛠️ Fitur Tambahan (Penugasan Mandiri)

Sesuai dengan instruksi tugas yang diberikan untuk mengembangkan fungsionalitas dari kode dasar praktikum, berikut adalah fitur-fitur yang ditambahkan:

### 1. Penambahan Kolom Input Password
* Menambahkan kolom input baru khusus untuk password pada `LoginPage`.
* Menerapkan properti `obscureText: true` pada bidang input tersebut agar karakter password yang diketik oleh pengguna secara otomatis disamarkan demi menjaga keamanan privasi.

### 2. Implementasi Validator Form
* Mengubah komponen `TextField` bawaan modul menjadi `TextFormField` dan membungkusnya ke dalam widget `Form` yang dikendalikan oleh `GlobalKey<FormState>`.
* **Validator Username:** Menambahkan sistem pengecekan agar kolom username tidak boleh dikosongkan saat menekan tombol login.
* **Validator Password:** Menambahkan logika validasi ganda, yaitu memastikan kolom password tidak boleh kosong dan **wajib diisi minimal sebanyak 6 karakter**. Jika kriteria ini tidak terpenuhi, sistem akan menampilkan pesan peringatan error berwarna merah dan menahan proses login.

---

## 🚀 Cara Menjalankan Proyek

1. Pastikan SDK Flutter sudah terpasang di komputer Anda.
2. Klona (*clone*) repositori ini:
   ```bash
   git clone [https://github.com/Rommy003/pertemuan10_2306019.git](https://github.com/Rommy003/pertemuan10_2306019.git)
