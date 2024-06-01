# Hasil Tantangan
## Data Tabel

![](aset/mysql72.png)

## Perubahan Struktur Tabel 

### Before
![](aset/mysql74.png)

### After
![](aset/mysql73.png)

## Perubahan Data Tabel 
### Before pegawai
![](aset/mysql72.png)

### After pegawai
![](aset/mysql78.png)

### Before cabang
![](aset/mysql79.png)

### After cabang 
![](aset/mysql80.png)

## Hasil Relasi 
![](aset/mysql77.png)


## Query Relasi dan Hasil

### Kode Program
```mysql
SELECT s.nama AS Nama_Siswa, n.nilai AS Nilai
FROM nilai AS n
INNER JOIN siswa AS s ON s.id = n.id_siswa
WHERE n.nilai > 75;
```

### Hasil
![](aset/mysql81.png)


