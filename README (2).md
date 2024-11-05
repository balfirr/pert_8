
# Cara Kerja Login Ionic
1. Pembuatan Formulir Login di Ionic dengan dua field input, seperti username/email dan password dan dapat dibuat menggunakan komponen Ionic, seperti <ion-input> untuk menerima masukan dari pengguna. Ketika pengguna mengisi formulir dan menekan tombol Login, aplikasi akan mengambil data yang dimasukkan dan mengirimkannya ke backend.
2. Ketika tombol login diklik, aplikasi akan mengambil data yang diisi pengguna (username dan password) dan mengirimkannya ke server melalui HTTP request (biasanya metode yang digunakan adalah POST karena berfungsi mengirimkan data secara aman) lalu setelah itu data akan dikirimkan ke server dalam format JSON melalui URL API endpoint
3. Setelah server menerima permintaan login, server akan memproses data tersebut. Server kemudian akan memeriksa apakah username dan password sesuai dengan data di database. Jika sesuai, server akan mengirimkan token autentikasi (biasanya token JWT atau sesi ID) sebagai tanda bahwa login berhasil. Jika tidak sesuai, server akan mengembalikan pesan kesalahan, misalnya "Invalid username or password".
4. Aplikasi Ionic menerima respons dari server. Jika login berhasil, aplikasi akan mendapatkan token autentikasi. Token ini kemudian akan disimpan di penyimpanan lokal (localStorage atau Ionic Storage) agar bisa digunakan pada permintaan selanjutnya.
5. Setelah login berhasil dan token disimpan, aplikasi dapat mengakses halaman-halaman yang membutuhkan autentikasi. Setiap kali aplikasi perlu mengakses data yang membutuhkan autentikasi (misalnya data profil pengguna), aplikasi akan mengirim token tersebut bersama dengan permintaan HTTP sebagai bukti bahwa pengguna telah login. Kemudian server akan memverifikasi token tersebut apakah token yang diterima valid atau tidak. Jika token valid, server akan mengizinkan akses ke data atau halaman tersebut. Jika token tidak valid, server akan mengembalikan status 401 Unauthorized, dan aplikasi bisa meminta pengguna untuk login kembali.
6. Proses logout biasanya hanya menghapus token dari penyimpanan lokal. Dengan begitu, pengguna tidak bisa lagi mengakses halaman yang terproteksi sampai mereka login kembali.
## Screenshots

![App Screenshot](https://github.com/balfirr/pert7/blob/78747e1fa6240c8723c8c19e22a09959ff88d4a5/appcb/Screenshot%202024-10-30%20213253.jpg)

