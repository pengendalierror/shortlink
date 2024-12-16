# ShortLink - URL Shortener Application

ShortLink adalah aplikasi pemendek URL dengan fitur multi-destination dan manajemen user berbasis PHP.

## Fitur

- Pembuatan shortlink dengan kode custom atau otomatis
- Multi-destination URL untuk satu shortlink
- Sistem autentikasi dengan approval admin
- Manajemen user (approve, reject, freeze/unfreeze)
- Statistik klik untuk setiap shortlink
- Session timeout untuk keamanan
- Responsive design dengan Material Design

## Persyaratan Sistem

- PHP 7.4 atau lebih tinggi
- MySQL 5.7 atau lebih tinggi
- Apache dengan mod_rewrite enabled
- SSL Certificate (disarankan untuk keamanan)

## Cara Install di Shared Hosting

1. **Persiapan Database**
   - Buat database baru di cPanel
   - Import file `database.sql` ke database yang baru dibuat
   - Catat nama database, username, dan password database

2. **Upload File**
   - Download semua file dari repository
   - Extract file ke komputer lokal
   - Edit file `config/database.php` dengan kredensial database:     ```php
     $db_host = 'localhost';
     $db_name = 'nama_database_anda';
     $db_user = 'username_database_anda';
     $db_pass = 'password_database_anda';     ```
   - Upload semua file ke public_html atau subdirektori melalui FTP/File Manager

3. **Konfigurasi .htaccess**
   - Pastikan file `.htaccess` terupload
   - Jika diinstall di subdirektori, edit file `.htaccess`:     ```apache
     RewriteBase /nama_subdirektori/     ```

4. **Pengaturan Permissions**
   - Set permission folder ke 755
   - Set permission file ke 644
   - Khusus folder yang perlu write access (jika ada uploads), set ke 777

5. **Akun Default**
   - Username: admin
   - Password: admin123
   - **PENTING**: Segera ubah password admin setelah login pertama kali

