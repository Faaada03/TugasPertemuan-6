# TugasPertemuan-6
# CRUD Barang Swalayan dengan Java Swing

## Deskripsi
Proyek ini adalah implementasi sederhana dari operasi **CRUD** (Create, Read, Update, Delete) untuk mengelola data barang swalayan menggunakan **Java Swing** dan **PostgreSQL**.  
Berbeda dari implementasi sebelumnya yang menggunakan satu `JFrame` saja, kali ini setiap fungsi CRUD dipisahkan ke dalam **`JDialog`**:
- `Insert` → menambah data baru  
- `Update` → memperbarui data yang sudah ada  
- `Delete` → konfirmasi penghapusan data  

Dengan pendekatan ini, antarmuka menjadi lebih bersih, terfokus, dan mudah digunakan.

## Fitur
- **Insert**: Tambah data barang baru lewat `JDialog Insert`.  
- **Update**: Edit data barang yang dipilih lewat `JDialog Update`.  
- **Delete**: Konfirmasi hapus data lewat `JDialog Delete`.  
- **Clear**: Hapus semua data barang sekaligus.  
- Tabel barang diperbarui secara otomatis setiap ada perubahan.  

## Teknologi
- **Java Swing** (GUI)  
- **PostgreSQL** (database)  
- **JDBC** (koneksi Java ke database)  

## Cara Menjalankan
1. Pastikan sudah menginstal **PostgreSQL** dan membuat database, misalnya:
   ```sql
   CREATE DATABASE DB_PBO_PRAK5;
   ```
2. Buat tabel `barang`:
   ```sql
   CREATE TABLE barang (
       no_seri VARCHAR(50) PRIMARY KEY,
       nama_barang VARCHAR(100),
       jenis VARCHAR(50),
       jumlah INT
   );
   ```
3. Ubah konfigurasi koneksi di file `ConnectCURD.java` sesuai database Anda:
   ```java
   String url = "jdbc:postgresql://localhost:5432/DB_PBO_PRAK5";
   String user = "postgres";
   String pass = "PASSWORD_ANDA";
   ```
4. Jalankan aplikasi lewat IDE (misalnya **NetBeans**) atau command line.

## Kesimpulan
Proyek ini menunjukkan bagaimana memisahkan fungsi CRUD ke dalam `JDialog` yang berbeda dapat membuat aplikasi lebih terstruktur dan jelas. Desain ini juga bisa menjadi dasar untuk pengembangan aplikasi yang lebih kompleks di masa depan.  
