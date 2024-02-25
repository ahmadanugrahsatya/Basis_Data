# instalase mysql

## Menggunakan XAMPP
1. buka XAMPP

![](aset/mysql1.png)

2. klik start di bagian mysql

![](aset/mysql2.png)

3. klik shell

![](aset/mysql3.png)

4. ketik mysql -u root -p lalu enter

![](aset/mysql4.png)

5. nanti nya akan muncul seperti ini

![](aset/mysql5.png)

6.  jika setelah di enter maka dibagian tersebut tidak perlu diisi langsung saja klik enter lagi

![](aset/mysql6.png)
## referensi video youtube
<https://youtu.be/tSGKZ_oaJOo?si=XhKflnx-D2Tq28Uv>

## Penggunaan awal mysql 

 query
  ```bash
mysql -u root -p
```

hasil

![](aset/mysql6.png)

analis
1. `mysql`  digunakan untuk memberitahu sistem bahwa aplikasi yang ingin di gunakan yaitu mysql
2. `-u `digunakan untuk membuat username dengan query nya -u
3. `root` merupakan sebuah username yang digunakan untuk masuk ke dalam aplikasi xampp
4. `-p` diguanakan untuk mengindikasi bahwa sistem harus meminta kita untuk mamasukkan kata sandi

kesimpulan
kesimpulannya adalah query `mysql -u root -p` digunakan untuk masuk ke dalam aplikasi mysql melalui aplikasi xampp, dan juga untuk `-u` membuat username.

# DataBase

## Membuat database 
yaitu dengan cara mengetikkan query `create database (nama database);` contoh seperti ini `create database angga_database;` maka nanti akan muncul seperti ini jika database telah terbuat.

![](aset/mysql7.png)
## Menampilkan database
untuk caranya kalian bisa mengetikkan query `show databases;`. penyebab mengapa ada tambahan huruf s di akhir kata database yaitu karena jika kalian mengetikkan `show databases;` maka yang akan di tampilakan ialah semua database yang, ada akan tetapi jika kita mengetikkan `show database;` maka yang tejadi ialah eror.

![](aset/mysql8.png)
## Menghapus database
kalian bisa menggukan cara yaitu mengetikkan query `drop database (nama database);` contoh seperti `drop database angga_database;` maka nanri akan muncul seperti ini jika database berhasil terhapus

![](aset/mysql9.png)
## Gunakan database
kalian bisa melakukannya dengan cara mengetikkan query `use nama database;` contoh seperti `use angga_database;` maka nanti akan muncul seperti ini jika database telah di buat

![](aset/mysql11.png)
 
 >[!faq] `database_1` bisa di akses padahal telah di hapus karena `database_1` telah dibuat ulang
 
 
## Tipe data

## angka 
Tipe data angka dalam MySQL digunakan untuk menyimpan nilai numerik. Berikut adalah definisi untuk beberapa tipe data angka umum dalam MySQL:

1. **INT atau INTEGER**: Tipe data ini digunakan untuk menyimpan bilangan bulat tanpa koma dengan panjang standar 4 byte. Contohnya, `INT(10)`.
    
2. **TINYINT**: Tipe data ini digunakan untuk menyimpan bilangan bulat kecil dengan panjang 1 byte. Contohnya, `TINYINT(3)`.
    
3. **SMALLINT**: Digunakan untuk menyimpan bilangan bulat dengan panjang 2 byte. Contohnya, `SMALLINT(5)`.
    
4. **MEDIUMINT**: Tipe data ini digunakan untuk menyimpan bilangan bulat dengan panjang 3 byte. Contohnya, `MEDIUMINT(8)`.
    
5. **BIGINT**: Tipe data ini digunakan untuk menyimpan bilangan bulat yang sangat besar dengan panjang 8 byte. Contohnya, `BIGINT(20)`.
    
6. **DECIMAL atau NUMERIC**: Tipe data desimal yang menyimpan angka berkoma dengan presisi dan skala yang dapat diatur. Contohnya, `DECIMAL(10,2)` untuk menyimpan angka dengan 10 digit, 2 di antaranya di belakang koma.
    
7. **FLOAT**: Digunakan untuk menyimpan angka berkoma dengan presisi ganda. Contohnya, `FLOAT(7,4)`.
    
8. **DOUBLE**: Tipe data ini mirip dengan FLOAT, namun dengan presisi yang lebih tinggi. Contohnya, `DOUBLE(15,8)`.
    
9. **BIT**: Tipe data boolean yang dapat menyimpan nilai 0 atau 1, atau NULL. Contohnya, `BIT(1)`.
    

Definisi tipe data ini mencakup panjang (length), presisi, dan skala yang memberikan kontrol lebih lanjut terhadap cara data angka disimpan.

## Teks
Dalam MySQL, terdapat beberapa tipe data teks yang digunakan untuk menyimpan data karakter atau string. Berikut adalah beberapa tipe data teks yang umum digunakan:

1. **CHAR(n)**: Menyimpan string karakter tetap (fixed-length) dengan panjang n. Jika panjang string kurang dari n, maka akan diisi dengan spasi. Misalnya, CHAR(10) akan menyimpan string dengan panjang tepat 10 karakter.
    
2. **VARCHAR(n)**: Menyimpan string karakter dengan panjang variabel (variable-length) maksimal n. Jika panjang string yang disimpan kurang dari n, maka hanya akan menggunakan ruang yang diperlukan. VARCHAR lebih efisien dalam penggunaan ruang dibandingkan CHAR.
    
3. **TEXT**: Menyimpan string karakter dengan panjang variabel yang sangat besar (hingga 65,535 karakter).
    
4. **TINYTEXT, MEDIUMTEXT, LONGTEXT**: Variasi dari tipe data TEXT dengan batasan panjang yang berbeda. TINYTEXT dapat menyimpan hingga 255 karakter, MEDIUMTEXT hingga 16,777,215 karakter, dan LONGTEXT hingga 4,294,967,295 karakter.
    
    

Tipe data teks ini memungkinkan Anda untuk menyimpan dan mengelola data karakter dengan berbagai cara sesuai kebutuhan, baik itu string dengan panjang tetap, variabel, atau dengan batasan panjang tertentu. Pemilihan tipe data tergantung pada karakteristik data yang akan disimpan.

## Tanggal
Dalam MySQL, terdapat beberapa tipe data yang digunakan untuk menangani tanggal dan waktu. Berikut adalah beberapa tipe data tanggal yang umum digunakan:

1. **DATE**: Menyimpan tanggal dengan format "YYYY-MM-DD". Tipe data ini tidak menyimpan informasi waktu, hanya tanggal.
    
    Contoh:
    `'2024-01-30'`

2. **TIME**: Menyimpan informasi waktu dengan format "HH:MM:SS". Tipe data ini tidak menyimpan tanggal, hanya waktu.    
    Contoh:
    `'14:30:00'`
    
3. **DATETIME**: Kombinasi dari DATE dan TIME. Menyimpan tanggal dan waktu dengan format "YYYY-MM-DD HH:MM:SS".
    Contoh:
    `'2024-01-30 14:30:00'`
    
4. **TIMESTAMP**: Mirip dengan DATETIME, tetapi dengan perbedaan utama dalam cara nilai-nilai default dan nilai saat direkam diperlakukan. Nilai TIMESTAMP secara otomatis diperbarui setiap kali baris diubah.
    
    Contoh:
    `'2024-01-30 14:30:00'`
    
5. **YEAR**: Menyimpan nilai tahun dengan format empat digit "YYYY". Digunakan terutama untuk menyimpan tahun.
    
    Contoh:
    `'2024'`
    

Tipe data tanggal ini memungkinkan pengelolaan informasi tanggal dan waktu dengan baik sesuai kebutuhan aplikasi yang menggunakan MySQL. Pemilihan tipe data yang tepat sangat bergantung pada jenis informasi waktu yang ingin Anda simpan dan bagaimana Anda berencana untuk menggunakannya.


## Boolean
Dalam MySQL, tipe data boolean umumnya diwakili oleh TINYINT(1), di mana nilai 0 menunjukkan "false" dan nilai selain 0 (biasanya 1) menunjukkan "true". Meskipun tipe data boolean tidak secara resmi didukung di MySQL sebelum versi 5.0.3, banyak aplikasi dan pengembang MySQL telah mengadopsi penggunaan TINYINT(1) untuk menyimpan nilai boolean.

Berikut adalah beberapa poin yang dapat membantu menjelaskan tipe data boolean dalam MySQL:

1. **TINYINT(1):** Pada dasarnya, MySQL tidak memiliki tipe data boolean yang jelas. Sebagai gantinya, konvensi umum adalah menggunakan kolom TINYINT(1) untuk menyimpan nilai boolean. Ukuran 1 di sini menunjukkan panjang kolom, dan karena itu, nilai yang diizinkan hanya 0 atau 1.
     Contoh:
    `CREATE TABLE contoh_boolean (     status TINYINT(1) );`
    
2. **0 dan 1:** Secara tradisional, nilai 0 sering diartikan sebagai "false" dan nilai 1 diartikan sebagai "true". Namun, beberapa aplikasi atau kasus penggunaan mungkin menggunakan nilai lain sebagai representasi boolean.
    
3. **NULL:** Nilai NULL juga dapat diizinkan untuk kolom TINYINT(1), yang berarti bahwa kolom tersebut tidak memiliki nilai boolean yang ditetapkan.
    Contoh:
    `INSERT INTO contoh_boolean (status) VALUES (NULL);`
    
4. **Boolean Functions:** MySQL menyediakan beberapa fungsi untuk bekerja dengan nilai boolean atau TINYINT(1), seperti `IF()`, `CASE`, dan fungsi-fungsi logika seperti `AND`, `OR`, dan `NOT`.
    Contoh:
    `SELECT IF(status = 1, 'Aktif', 'Tidak Aktif') AS status_text FROM contoh_boolean;`
    
5. **Penanganan Tipe Data Boolean di Aplikasi:** Saat menggunakan MySQL dengan bahasa pemrograman tertentu, aplikasi dapat menangani nilai boolean ini dengan lebih mudah, memberikan abstraksi tingkat tinggi untuk representasi boolean.
    

Perlu dicatat bahwa sejak MySQL versi 8.0.1, MySQL memperkenalkan tipe data BOOLEAN yang sebenarnya, tetapi di bawahnya, sebenarnya masih diimplementasikan sebagai TINYINT(1) untuk kompatibilitas mundur. Namun, dengan menggunakan BOOLEAN, kita dapat menambahkan keterangan semantik dan meningkatkan kejelasan dalam skema basis data.

## Tipe data pilihan
 ENUM: Menyimpan satu nilai dari daftar yang telah ditentukan sebelumnya. Setiap nilai ENUM memiliki indeks numerik yang terkait, dan nilai yang disimpan dalam tabel adalah indeks tersebut.
    
SET: Menyimpan satu set nilai dari daftar yang telah ditentukan sebelumnya. Nilai-nilai dalam SET diurutkan sesuai dengan urutan deklarasinya.


# Membuat Database
## Create Database
Cara untuk membuat database yaitu dengan cara 

Struktur Query
```mysql
create database nama_database;
```

Contoh Query
```mysql
create database rental_angga
```

hasil
![](aset/mysql12.png)

Analisis
1. `crate database rental_angga` adalah query yang yang digunakan untuk membuat table di mysql

> [!SUMMARY] Kesimpulan
> ketika ingin membuat sebuah database baru kita harus memasukkan sebuah query yaitu `create database nama_database;`


# Tabel
## Buat tabel
Cara membuat tabel di mysql kita bisa menggunakan sebuah query yaitu `create table nama_tabel(isian tabel);`

>[!note] sebelum ingin membuat tabel kalian sebaiknya membuat database dan masuk ke dalam database

Struktur Query
```mysql
CREATE TABLE [nama_table] (nama_kolom1 tipe_data(ukuran) [tipe_constraint], nama_kolom2 tipe_data(ukuran) [tipe_constraint], nama_kolom3 tipe_data(ukuran) [tipe_constraint] );
```
\contoh:
```mysql
create table pelanggan (id_pelanggan int(4) primary key not null, nama_depan varchar(25) not null, nama_belakang varchar(25), no_telpon char(12) unique);
```

hasil:
![](aset/mysql13.png)

Analisis:
1. `create table pelanggan` adalah code yang digunakan untuk membuat sebuah tabel baru dan **pelanggan** 
adalah nama tabel nya
2. `id_pelanggan`, `nama_depan`, `nama_belakang`, `no_telpon` merupakan judul kolom
3. `int(4)` merupakan tipe data angka dan 4 adalah jumlah maximal inputan
4. `varchar(25)` merupakan tipe data yang Menyimpan string karakter dengan panjang variabel (variable-length) maksimal n dan 25 adalah jumlah maksimal inputan
5. `char(12)` merupakan tipe data yang menyimpan string karakter tetap (fixed-length) dengan panjang n dan 12 adalah jumlah maksimal inputan
6. `primary key` sebagai identitas yang untuk membedakan setiap baris yang ada didalam suatu tabel
7. `unique` untuk memastikan bahwa setiap baris data yang terdapat dalam suatu tabel bersifat unik (tidak sama)

> [!SUMMARY] 
>Kesimpulannya adalah ketika kita ingin membuat tabel kalian bisa menggunakan struktur query `CREATE TABLE [nama_table] (nama_kolom1 tipe_data(ukuran) [tipe_constraint], nama_kolom2 tipe_data(ukuran) [tipe_constraint], nama_kolom3 tipe_data(ukuran) [tipe_constraint] );`

## Tampilkan struktur tabel
Cara untuk menampilkan struktur tabel yaitu dengan cara menggunakan query `desc (nama table);`

contoh:
```mysql
desc pelanggan;
```

hasil:
![](aset/mysql13.png)

analisis:
1. `desc pelanggan;` merupakan query yang di gunakan untuk menampilkan struktur tabel yang telah di buat dan pelanggan adalah nama dari tabelnya

> [!SUMMARY] Kesimpulan
> ketika kalian ingin membuat kalian bisa menggunakan query `desc nama_table`
## Menampilkan daftar table

Cara untuk  menampilkan daftar table yaitu dengan cara 

contoh
```mysql
show tables;
```

hasil:
![](aset/mysql14.png)

analisis:
1. `show tables;` adalah query yang digunakan untuk menampilkan daftar table yang telah dibuat

> [!SUMMARY] Kesimpulan
> ketika ingin melihat daftar table yang telah di buat kalian bisa menggunakan query `show tables;`
  
## QnA


>[!faq]- Mengapa hanya kolom id_pelanggan yang menggunakan constraint PRIMARY KEY?
>karena id_pelanggan karena ini adalah cara untuk mengidentifikasi setiap baris dalam tabel, dan juga primary key digunakan untuk memberikan hak istimewa dari sebuah kolom dan tidak dapat diduplikat oleh setiap baris.

>[!faq]- Mengapa pada kolom no_telp yang menggunakan tipe data char bukan varchar?
>karena tipe data char menyimpan string karakter tetap dan no_telp bersifat karakter tetap

>[!faq]- Mengapa hanya kolom no_telp yang menggunakan constraint UNIQUE?
>karena unique berfungsi untuk memastikan bahwa setiap baris data yang terdapat dalam suatu tabel bersifat unik (tidak sama) dan no_telp pasti tidak akan sama

>[!faq]- Mengapa kolom no_telp tidak memakai constraint NOT NULL, sementara kolom lainnya menggunakan constraint tersebut?
>Karena nomor telpon dianggap opsional. nomor telepon hanya menjadi wajib saat pengguna melakukan langkah-langkah tertentu, Anda mungkin tidak ingin mengharuskan pengguna mengisinya pada tahap awal.

>[!faq]- apa perbedaan primery key dan unique?
>kalau primery key untuk membedakan data yang sama dan hanya boleh 1 dan tidak boleh tidak ada. sedangkan unique sebuah kolom yang memiliki data yang berbeda atau tidak sama unique boleh 1,2,3 Dan 
>seterusnya dan boleh tidak ada.


# Insert
## Insert 1 data
### Struktur
```mysql
insert into [nama_table] values (nilai1, nilai2, nilai3,);
```

### Contoh
```mysql
insert into pelanggan values(1, 'Ahmad', 'Satya', '0895XXXX');
```

### Hasil
![](aset/mysql15.png)
### Analsis
1. `insert into` adalah query yang digunakan untuk menginput isi table
2. `pelanggan` adalah nama table nya
3. `values` adalah query yang digunakan untuk memasukkan nilai ke kolom
4. `(1, 'Ahmad', 'Satya', '0895XXXX')` nilai yang ingin di masukkan ke kolom
5. `;` penutup query

> [!Summary] Kesimpulan
> Jika ingin memasukkan sebuah nilai ke dalam tabel maka kalian bisa menggunakan query `insert into [nama_table] values(nilai1, nilai2, nilai3);`

## insert lebih dari 1 data 
### Struktur
```mysql
insert into [nama_table] values (nilai1, nilai2, nilai3,), (nilai4, nilai5, nilai6,);
```

### Contoh
```mysql
insert into pelanggan values(1, 'Ahmad', 'Satya', '0895XXXX'), (2, 'Daud', 'Resky', '0812XXXX'), (3, 'Resky', 'Alfatir', '0834XXXX'), (4, 'Agis', null , '0856XXXX');
```

 
![](aset/mysql16.png)

### Analisis
1. `insert into` query yang di gunakan untuk menginput isi table
2. `pelanggan` adalah nama table yang ingin di isi
3. `values` query yang di gunakan untuk memasukkan nilai ke kolom
4. `(1, 'Ahmad', 'Satya', '0895XXXX'), (2, 'Daud', 'Resky', '0812XXXX'), (3, 'Resky', 'Alfatir', '0834XXXX'), (4, 'Agis', null , '0856XXXX')` merupakan nilai yang akan di masukkan

> [!Summary] Kesimpulan
> jika ingin mengisi atau menginput kolom di mysql kalian bisa menggunakan query dengan struktur `insert into [nama_table] values (nilai1, nilai2, nilai3,), (nilai4, nilai5, nilai6,);`

## Menyebut Kolom

### Struktur
```mysql
insert into [nama_table](kolom1, kolom2, kolom3) values (nilai1, nilai2, nilai3);
```

### Contoh
```mysql
insert into pelanggan (id_pelanggan, nama_depan) values (5, "fahri")
```

### Hasil

![](aset/mysql17.png)

### Analisis
1. `insert into` query yang digunakan untuk menginput isi table
2. `pelanggan` adalah nama table yang ingin di isi
3. `(id_pelanggan, nama_depan)` nama kolom yang hanya akan di isi
4. `values` query yang di gunakan untuk memasukkan nilai ke kolom
5. `(5, "fahri")` merupakan nilai yang akan di masukkan

> [!Summary] Kesimpulan
>jika ingin memasukkan nilai yang hanya ke kolom tertentu kalian bisa pakai sebuah query yang strukutur nya  `insert into [nama_table](kolom1, kolom2, kolom3) values (nilai1, nilai2, nilai3);`

# Select

## Seluruh Data
### Struktur

```mysql
Select * from [nama_table]
```

### Contoh
```mysql
select * from pelanggan;
```

### Hasil
![](aset/mysql18.png)

### Analisis
1. `Select` merupakan query yang digunakan untuk menampilkan hasil `insert` 
2. `*` artinya semua kolom yang ada di table akan di tampilkan 
3. `from` query yang digunakan untuk memberikan penanda bahwa table mana yang akan di tampilkan
4. `pelanggan` merupakan nama table yang isi nya akan di tampilkan

> [!summary] Kesimpulan
> jika ingin menampilkan hasil dari insert kalian bisa menggunakan query yaitu dengan struktur `Select * from [nama_table]`

## Data Kolom Tertentu 
### Struktur 

```mysql
select [nama_kolom1], [nama_kolom2], mysqlolom_n]
```

### Contoh
```mysql
select nama_depan from pelanggan;
```

### Hasil
![](aset/mysql19.png)

### Analisis

1. `Select` merupakan query yang digunakan untuk menampilkan hasil `insert` 
2. `nama_depan`  adalah nama kolom yang akan di tampilkan
3. `from` query yang digunakan untuk memberikan penanda bahwa table mana yang akan di tampilkan
4. `pelanggan` merupakan nama table yang isi nya akan di tampilkan
## Klausa WHERE 
### Struktur
```mysql
select [nama_kolom] form pelanggan [nama_table] where[kondisi];
```

### Contoh
```mysql
select id_pelanggan, nama_depan from pelanggan where id_pelanggan=2;
```

### Hasil
![](aset/mysql20.png)

### Analisis
1. `select` merupakan query yang digunakan untuk menampilkan hasil `insert` 
2. `id_pelanggan, nama_depan` adalah nama kolom yang akan di tampilkan
3. `from` adalah penanda yang digunakan untuk menandakan table mana yang akan di tampilkan
4. `pelanggan` adalah nama table yang akan di tampilkan
5. `where` adalah query yang digunakan untuk memberikan sebuah kondisi 
6. `id_pelanggan=2` adalah sebuah kondisi yang telah di berikan

> [!summary]
> jika ingin menampilkan baris yaitu dengan query yang dengan struktur `select [nama_kolom] form pelanggan [nama_table] where[kondisi];`
# Update

## Struktur
```mysql
update nama_table set nama_kolom where kondisi;
```

## Contoh

```mysql
update pelanggan set no_telpon="0801XXXX" where id_pelanggan="1";
``` 

## Hasil
![](aset/mysql21.png)


## Analisis
1. `update` adalah query yang digunakan untuk memperbarui nilai dari kolom
2. `pelanggan` nama table yang akan di perbarui nilai kolomnya
3. `set` query yang digunakan untuk memberikan penanda bahwa yang nilainya akan di rubah 
4. `no_telpon` kolom yang akan di ubah nilai nya
5. `"0801XXXX"` nilai yang akan dimasukkan 
6. `where` query yang digunakan untuk memberikan sebuah kondisi

> [!summary] Kesimpulan
> jika ingin mengubah atau mengupdate sebuah table kalian bisa menggunakan query `update` dengan struktur query yaitu `update nama_table set nama_kolom where kondisi;`


# Delete

## Struktur

```mysql
delete from nama_table where kondisi;
```

## Contoh

```mysql
delete from pelanggan where id_pelanggan=5;
```

## Hasil
![](aset/mysql22.png)

## Analisis
1. `delete` query yang digunakan untuk menghapus baris kolom
2. `from` query yang digunakan untuk memberikan penanda bahwa table mana yang akan di hapus baris nya
3. `pelanggan` nama table yang akan di hapus baris nya
4. `where` query yang digunakan untuk memberikan sebuah kondisi
5. `id_pelanggan` nama kolom nya 
6. `=` operatornya
7. `5` nilai nya

> [!summary] Kesimpulan
> jika ingin menghapus baris table kalian bisa menggunakan query `delete` dengan struktur yaitu `delete from nama_table where kondisi;`


# Drop Table

## Struktur 
```mysql
Drop table [nama_table];
```

## Contoh
```mysql
drop table pelanggan;
```

## Hasil
![](aset/mysql23.png)

## Analisis
1. `drop table` query yang digunakan untuk menghapus sebuah table
2. `pelanggan` merupakan nama table yang akan di hapus


> [!summary] Kesimpulan
> jika ingin menghapus table kalian bisa menggunakan query  `drop` dengan struktur query yaitu `drop table [nama_table];`


 