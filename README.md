# Pertemuan 10 - Local Storage Menggunakan SharedPreferences

Repositori ini dibuat untuk memenuhi tugas Praktikum Pemrograman Mobile - Modul 10 mengenai implementasi penyimpanan data lokal (*local storage*) pada aplikasi Flutter menggunakan *package* `shared_preferences`.

## 📌 Pembahasan Singkat Praktikum

Pada modul ke-10 ini, materi berfokus pada konsep dasar penyimpan data di dalam memori internal perangkat pengguna tanpa memerlukan koneksi internet. Beberapa poin utama yang dipelajari meliputi:

1. **Konsep & Fungsi Local Storage:** Berfungsi untuk menjaga persistensi data sederhana seperti sesi login (*session*), preferensi tema aplikasi (*dark/light mode*), pengaturan aplikasi, maupun *cache data*.
2. **SharedPreferences:** Pemanfaatan *package* `shared_preferences` untuk menyimpan data sederhana berbasis pasangan kunci-nilai (*key-value pair*). Tipe data yang didukung antara lain `String`, `int`, `double`, `boolean`, dan `List<String>`.
3. **Alur Autentikasi Lokal:** * **Login:** Mengubah status `isLogin` menjadi `true` dan menyimpan teks `username` ke memori lokal.
   * **Auto-Login Check:** Saat aplikasi pertama kali dibuka (`main.dart`), sistem memeriksa status `isLogin`. Jika bernilai `true`, pengguna langsung diarahkan ke `HomePage` tanpa harus melewati `LoginPage` lagi.
   * **Logout:** Menghapus seluruh data sesi yang tersimpan (`prefs.clear()`) dan mengembalikan pengguna ke `LoginPage`.

---

## 🛠️ Fitur Tambahan (Penugasan Mandiri)

Sebagai bagian dari pengembangan mandiri dan pemenuhan tugas, terdapat beberapa modifikasi penting pada komponen antarmuka dan logika autentikasi:

### 1. Perbaikan Tata Letak Profil (`HomePage`)
* Mengubah susunan baris dan kolom agar **Ikon Verified** (centang hijau) berada rapi tepat di bawah teks sambutan ("Welcome, [username]"), sejajar di samping teks *username* utama.
* Menerapkan `CrossAxisAlignment.start` agar seluruh informasi teks profil bergeser rapi ke sebelah kiri di samping foto avatar.

### 2. Penambahan Kolom Password & Validasi (`LoginPage`)
* **Form Validation:** Mengubah komponen `TextField` bawaan modul menjadi `TextFormField` dan membungkusnya dengan widget `Form` serta `GlobalKey<FormState>`.
* **Kolom Password:** Menambahkan input khusus password yang dilengkapi fitur `obscureText: true` agar karakter yang diketik pengguna tersamarkan (menjadi titik-titik).
* **Fungsi Validator:**
  * Menambahkan validasi pada kolom *Username* (tidak boleh kosong).
  * Menambahkan validasi pada kolom *Password* (tidak boleh kosong dan **minimal harus berjumlah 6 karakter**). Jika input tidak sesuai, aplikasi akan menampilkan pesan error berwarna merah di bawah kolom input dan menahan proses perpindahan halaman.

---

## 🚀 Cara Menjalankan Proyek

1. Pastikan Anda telah memasang SDK Flutter di perangkat Anda.
2. Klona (*clone*) repositori ini ke komputer lokal Anda:
   ```bash
   git clone [https://github.com/Rommy003/pertemuan10_2306019.git](https://github.com/Rommy003/pertemuan10_2306019.git)
