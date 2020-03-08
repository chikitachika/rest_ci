# Laporan Workshop WEB Framework
Pada minggu ke-3 kami melakukan praktikum yaitu mengaplikasikan GET, POST, Put dan DELETE dengan RestAPI.

## Bahan dan Alat

- Komputer / Laptop
- XAMPP
- Visual Studio Code
- Postman
- Wifi / Internet

## Installation

```sh
composer require chriskacerguis/codeigniter-restserver
```

## Cara Install Postman :
1. Download aplikasi di https://www.postman.com/downloads/
2. Setelah didownload lalu lakukan instalasi.
3. Jika sudah terinstall silakan bukan postman lalu sign in dengan akun google.



## Langkah

1. Persiapkan terlebih dahulu Webserver seperti Xampp, Wampp, atau lainnya.

2. Unduh Codeigniter dan library REST server pada link https://github.com/ardisaurus/ci-restserver.

3. Setelah semua yang diperlukan telah siap, extract Codeigniter dan library REST server yang telah didownload dan pindah ke htdocs pada direktori xampp lalu rename folder Codeigniter dan library REST server menjadi rest_ci.

4. Untuk mengecek apakah instalasinya berhasil maka lanjutkan buka di browser dengan mengetikan address http://127.0.0.1/rest_ci/index.php/rest_server.

5. Selanjutnya lakukan konfigurasi database. Buat DB baru dengan nama "kontak"; (CREATE DATABASE kontak;).

6. Buat tabel baru dengan nama "telepon" dengan field id (int 11 AUTO_INCREMENT), nama (varchar 30), nomor (varchar 11).

7. Masukkan data ke dalam tabel, contohnya (1, 'Orion', '08576666762').

8. Buka database.php pada rest_ci/application/config ubah menjadi 
    - 'hostname' => 'localhost',
    - 'username' => 'root',
    - 'password' => '', *bisa dikosongkan
    - 'database' => 'kontak', *nama DB

9. Selanjutkan ke metode GET. Metode GET menyediakan akses baca pada sumber daya yang disediakan oleh REST API. Sebagai contohnya digunakan untuk membaca data dari tabel telepon pada database kontak. Buat file php baru di di rest_ci/application/controller dengan nama kontak.php. Contoh codenya bisa dilihat di file kontak.php.

10. Untuk menguji kode yang telah dibuat buka Postman, Pilih metode GET, masukan http://127.0.0.1/rest_ci/index.php/kontak pada address bar lalu klik "Send".

11. Ubah address pada address bar menjadi http://127.0.0.1/rest_ci/index.php/kontak?id=7 lalu klik "Send". Maka hanya data dengan id 7 yang akan muncul.

12. Selanjutnya menggunakan metode POST Metode POST digunakan untuk mengirimkan data baru dari client ke server REST API. Sebagai contohnya digunakan untuk menambahkan kontak baru yang terdiri dari id, nama, dan nomor. Contoh codenya bisa dilihat di file kontak.php
Sebagai contoh, saya membuat id (3), Nama (ana), nomor (0852656146547).

13. Untuk mengujinya buka Postman, pilih metode POST, masukan http://127.0.0.1/rest_ci/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key dan value yang diperlukan (id, nama, nomor), lalu klik "Send".

14. Lalu Lakukan metode GET untuk melihat data terbaru.

15. Selanjutnya menggunakan metode PUT. Metode PUT digunakan untuk memperbarui data yang telah ada di server REST API. Contoh codenya bisa dilihat di file kontak.php

16. Untuk mengujinya buka Postman, pilih metode PUT, masukan http://127.0.0.1/rest_ci/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan diubah diikuti key dan value selanjutnya, lalu klik "Send". Lakukan metode GET untuk melihat data terbaru.

17. Selanjutnya menggunakan metode DELETE. Metode DELETE digunakan untuk menghapus data yang telah ada di server REST API. Contoh codenya bisa dilihat di file kontak.php.

18. Untuk mengujinya buka Postman, pilih metode DELETE, masukan http://127.0.0.1/rest_ci/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan dihapus, sebgai contoh saya mencoba untuk menghapus yang ber-id (3) lalu klik "Send". Lakukan metode GET untuk melihat data terbaru.

19. Sekian Terimakasih.

## Daftar Pustaka
- BKPM Workshop WEB Framework
- https://www.codepolitan.com/rest-api-server-sederhana-dengan-codeigniter-58901f324a29f
