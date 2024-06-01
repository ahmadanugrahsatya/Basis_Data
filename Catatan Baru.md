# Query 4
```mysql
SELECT ProductsID FROM products UNION SELECT ProductID FROM OrderDetails;
```


![[Pasted image 20240514132843.png]]

- SELECT untuk memilih kolom mana saja Yang ingin ditampilkan dan dari tabel mana kolom tersebut dipilih.
- Product ID: Adalah nama kolom yang dipilih unutk digabungkan .
- From Products = untuk memilih dari tabel mana saja data kolomnya akan digabung.
- UNION = untuk melakukan dua SELECT, data Yang tampil adalah hasil gabungan dari tobel Products dengan OrderDetails. Tapi tampilannya tidak menampil duplikat dan banča tampilan Distinct (Harta menampilkan masing-masing Satu).
- SELECT untuk memilih kolam apa saja yang ingin ditampilkan
- ProductID= adalah nama kolom yang dipilih untuk digabungkan.
- From soles untur memilih dari tabel mana sara Xing data kolonnya akan dibaland Hasilnya merupakan hasil Sabundan dari tabel Productsdummy dan Sales Farom ProductID merupakan kolam Yang datanya dilabuni namun data duplikać terhapus/tidak ditampilkan karena tampilan undan adalah Distinct


# Query 5

```mysql
SELECT ProductID FROM products UNION ALL SELECT ProductID FROM OrderDetails;
```

## Hasil

![[Pasted image 20240514133254.png]]


![[Pasted image 20240514133212.png]]
- SELECT = untuk memilih kolom mana saja yang ingin ditampilkan/digabung.
- FROM Products = untuk memilih dari tabel mana saja yang data kolomnya akan digabung
- ProductID = adalah nama kolom yang dipilih untuk digabungkan
- UNION ALL = untuk menggabung suatu kolom dan tabel. Dan menampilkan semua Data termasuk yang duplikat.
- SELECT = untuk memilih kolom mana saja yang ingin di tampilkan/digabung
- ProductID = adalah nama kolom yang dipilih untuk digabungkan
- FROM OrderDetails = untuk memilih dari tabel mana saja yang data kolomnya akan digabung   
- Hasilnya = semua data termasuk data duplikat akan di tampilkan semua. Dari tabel Products dan OrderDetails

# Query 6
## Kode Program
```mysql
SELECT ProductID FROM products INTERSECT SELECT ProductID FROM OrderDetails;
```


## Hasil
![[Pasted image 20240514133443.png]]

- SELECT = untuk memilih kolom mana saja yang ingin ditampilkan/digabung
- Product ID = adalah nama kolam Yand dipilih untut digabungkan.
- From Products = untuk memilih dari tabel mana saja yang data kolomnya akan digabung
- INTERSECT = untut menampilkan gabungan dari tabel Products dan OrderDetails tapi hanya data Yang Sama/identik
- SELECT = untuk memilih kolom mana saja yang ingin ditampilkan / digabung 
- ProductID= adalah nama kolom Yang dipilih untuk digabungkan.
- From OrderDetails = untuk memilih dari tabel mana saja yang data kolamnya akan digabung
- Hasilnya  = hanya data yang sama dengan antarkolom pada dua tabel yang tampil.