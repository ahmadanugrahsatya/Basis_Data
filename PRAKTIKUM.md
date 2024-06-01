# QUERY 1
```SQL
SELECT p.ProductID, p.ProductName, od.Quantity, p.UnitsInStock
    -> FROM Products p
    -> INNER JOIN OrderDetails od ON p.ProductID = od.ProductID
    -> ORDER BY p.ProductID ASC;
```
## HASIL
![[Screenshot_20240601-124647_Termux.jpg]]

### ANALISIS 
1. **SELECT p.ProductID, p.ProductName, od.Quantity, p.UnitsInStock**

- Bagian ini menentukan kolom-kolom yang akan ditampilkan dalam hasil query. Kolom-kolom tersebut adalah:
    - `p.ProductID`: ID produk dari tabel `Products`.
    - `p.ProductName`: Nama produk dari tabel `Products`.
    - `od.Quantity`: Jumlah produk yang dipesan dari tabel `OrderDetails`.
    - `p.UnitsInStock`: Jumlah unit produk yang tersedia di stok dari tabel `Products`

2. **FROM Products p**
    
    - Bagian ini menentukan tabel utama yang digunakan dalam query, yaitu tabel `Products`. Alias `p` digunakan untuk mempermudah referensi ke tabel ini.

3.  **INNER JOIN OrderDetails od ON p.ProductID = od.ProductID**
    
    - Bagian ini menghubungkan tabel `Products` dengan tabel `OrderDetails` menggunakan klausa `INNER JOIN`. Hubungan dibuat berdasarkan kolom `ProductID` yang ada di kedua tabel tersebut.
    - Alias `od` digunakan untuk tabel `OrderDetails`.

4. **ORDER BY p.ProductID ASC**
    
    - Bagian ini menentukan urutan hasil query berdasarkan kolom `ProductID` dari tabel `Products` secara ascending (menaik).

### Penjelasan Fungsionalitas

Query ini mengambil data dari dua tabel: `Products` dan `OrderDetails`. Untuk setiap produk yang memiliki entri dalam tabel `OrderDetails`, query ini akan menampilkan:

- ID produk (`ProductID`)
- Nama produk (`ProductName`)
- Jumlah produk yang dipesan (`Quantity`)
- Jumlah unit produk yang tersedia di stok (`UnitsInStock`)

Hasil query kemudian diurutkan berdasarkan `ProductID` secara ascending.

# QUERY 2

```sql
SELECT p.ProductID, p.ProductName, p.UnitPrice, od.Quantity, p.UnitsInStock
    -> FROM Products p
    -> LEFT OUTER JOIN OrderDetails od
    -> ON p.ProductID = od.ProductID
    -> ORDER BY p.ProductID ASC;
```
## HASIL 
![[Screenshot_20240601-125812_Termux.jpg]]
## ANALISIS 
1. **SELECT p.ProductID, p.ProductName, p.UnitPrice, od.Quantity, p.UnitsInStock**
    
    - Bagian ini menentukan kolom-kolom yang akan ditampilkan dalam hasil query. Kolom-kolom tersebut adalah:
        - `p.ProductID`: ID produk dari tabel `Products`.
        - `p.ProductName`: Nama produk dari tabel `Products`.
        - `p.UnitPrice`: Harga unit produk dari tabel `Products`.
        - `od.Quantity`: Jumlah produk yang dipesan dari tabel `OrderDetails`. Jika tidak ada pesanan untuk produk tertentu, nilai ini akan `NULL`.
        - `p.UnitsInStock`: Jumlah unit produk yang tersedia di stok dari tabel `Products`.
2.  **FROM Products p**
    
    - Bagian ini menentukan tabel utama yang digunakan dalam query, yaitu tabel `Products`. Alias `p` digunakan untuk mempermudah referensi ke tabel ini.
3.  **LEFT OUTER JOIN OrderDetails od ON p.ProductID = od.ProductID**
    
    - Bagian ini menghubungkan tabel `Products` dengan tabel `OrderDetails` menggunakan klausa `LEFT OUTER JOIN`. Hubungan dibuat berdasarkan kolom `ProductID` yang ada di kedua tabel tersebut.
    - Alias `od` digunakan untuk tabel `OrderDetails`.
    - `LEFT OUTER JOIN` memastikan semua baris dari tabel `Products` akan ditampilkan, bahkan jika tidak ada entri yang sesuai di tabel `OrderDetails`. Jika tidak ada kecocokan, kolom dari tabel `OrderDetails` (seperti `Quantity`) akan mengandung nilai `NULL`.

4. **ORDER BY p.ProductID ASC**
    
    - Bagian ini menentukan urutan hasil query berdasarkan kolom `ProductID` dari tabel `Products` secara ascending (menaik).

### Penjelasan Fungsionalitas

Query ini mengambil data dari dua tabel: `Products` dan `OrderDetails`. Untuk setiap produk, query ini akan menampilkan:

- ID produk (`ProductID`)
- Nama produk (`ProductName`)
- Harga unit produk (`UnitPrice`)
- Jumlah produk yang dipesan (`Quantity`, jika ada; jika tidak, akan bernilai `NULL`)
- Jumlah unit produk yang tersedia di stok (`UnitsInStock`)

Hasil query kemudian diurutkan berdasarkan `ProductID` secara ascending.

# QUERY 3

```sql
SELECT p.ProductID, p.ProductName, p.UnitPrice, od.Quantity, p.UnitsInStock
    -> FROM Products p
    -> RIGHT OUTER JOIN OrderDetails od
    -> ON p.ProductID = od.ProductID
    -> ORDER BY p.ProductID ASC;
```
## HASIL 
![[Screenshot_20240601-130507_Termux.jpg]]

## ANALISIS 
1. **SELECT p.ProductID, p.ProductName, p.UnitPrice, od.Quantity, p.UnitsInStock**
    
    - Bagian ini menentukan kolom-kolom yang akan ditampilkan dalam hasil query. Kolom-kolom tersebut adalah:
        - `p.ProductID`: ID produk dari tabel `Products`.
        - `p.ProductName`: Nama produk dari tabel `Products`.
        - `p.UnitPrice`: Harga unit produk dari tabel `Products`.
        - `od.Quantity`: Jumlah produk yang dipesan dari tabel `OrderDetails`.
        - `p.UnitsInStock`: Jumlah unit produk yang tersedia di stok dari tabel `Products`.
2. **FROM Products p**
    
    - Bagian ini menentukan tabel utama yang digunakan dalam query, yaitu tabel `Products`. Alias `p` digunakan untuk mempermudah referensi ke tabel ini.
3. **RIGHT OUTER JOIN OrderDetails od ON p.ProductID = od.ProductID**
    
    - Bagian ini menghubungkan tabel `Products` dengan tabel `OrderDetails` menggunakan klausa `RIGHT OUTER JOIN`. Hubungan dibuat berdasarkan kolom `ProductID` yang ada di kedua tabel tersebut.
    - Alias `od` digunakan untuk tabel `OrderDetails`.
    - `RIGHT OUTER JOIN` memastikan semua baris dari tabel `OrderDetails` akan ditampilkan, bahkan jika tidak ada entri yang sesuai di tabel `Products`. Jika tidak ada kecocokan, kolom dari tabel `Products` (seperti `ProductID`, `ProductName`, `UnitPrice`, dan `UnitsInStock`) akan mengandung nilai `NULL`.
4. **ORDER BY p.ProductID ASC**
    
    - Bagian ini menentukan urutan hasil query berdasarkan kolom `ProductID` dari tabel `Products` secara ascending (menaik). Namun, karena `ProductID` dari tabel `Products` dapat bernilai `NULL` jika tidak ada kecocokan, hasil urutannya mungkin tidak sepenuhnya intuitif.

### Penjelasan Fungsionalitas

Query ini mengambil data dari dua tabel: `Products` dan `OrderDetails`. Untuk setiap entri di tabel `OrderDetails`, query ini akan menampilkan:

- ID produk (`ProductID`)
- Nama produk (`ProductName`)
- Harga unit produk (`UnitPrice`)
- Jumlah produk yang dipesan (`Quantity`)
- Jumlah unit produk yang tersedia di stok (`UnitsInStock`)

Jika tidak ada kecocokan di tabel `Products` untuk entri di tabel `OrderDetails`, kolom dari tabel `Products` akan bernilai `NULL`.

Hasil query kemudian diurutkan berdasarkan `ProductID` dari tabel `Products` secara ascending. Namun, karena `RIGHT OUTER JOIN` digunakan, urutan `ProductID` dapat mengandung nilai `NULL`.