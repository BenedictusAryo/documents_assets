# 10 Merging with VLOOKUP in Data Science 2

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pertama pada video ini kita akan menangani spasi. Nah, pada data kita pada data pertama yaitu mari kita handle spasi
```
data_kelamin['Nama'] = data_kelamin['Nama'].str.strip()
data_kelamin.head()
```
*Output :*

| Nama    | Kelamin   | NIM      |
|---------|-----------|----------|
| Andi  S | Laki-laki | 14611155 |
| Iva     | Perempuan | 14611156 |
| Ihsan   | Laki-laki | 14611157 |
| Dewi    | Perempuan | 14611158 |
| Kurnia  | Perempuan | 14611159 |

Memilih dan menghapus kolom. Nak kali ini kita memilih data pada sheet Kelamin untuk variabel ```Nama``` dan ```Kelamin```. 
```
data_kelamin[['Nama','Kelamin']]
```
*Output :*

| Nama    | Kelamin   |
|---------|-----------|
| Andi  S | Laki-laki |
| Iva     | Perempuan |
| Ihsan   | Laki-laki |
| Dewi    | Perempuan |
| Kurnia  | Perempuan |

Jika tidak ingin menghapus kolom untuk data yang kita gunakan selanjutnya dengan menggunakan ```.drop```. Misalnya kita menghapus kolom Kelamin
```
data_kelamin.drop('Kelamin', axis=1)
```
*Output :*

| Nama    | NIM      |
|---------|----------|
| Andi  S | 14611155 |
| Iva     | 14611156 |
| Ihsan   | 14611157 |
| Dewi    | 14611158 |
| Kurnia  | 14611159 |
| Eko     | 14611160 |
| Tika    | 14611161 |
| Fitri   | 14611162 |
| Gita    | 14611163 |
| Hafidz  | 14611164 |
| Maya    | 14611165 |
| Lukman  | 14611166 |
| April   | 14611167 |
| Eka     | 14611168 |
| Wati    | 14611169 |

Setelah analisis diatas kita akan menggabungkan 2 sheet yang kita punya dengan menggunakan  ```.merge()```
```
data_kelamin.merge(data_nilai, on='Nama', how='left')
````
*Output :*

| Nama    | Kelamin   | NIM      | Nilai |
|---------|-----------|----------|-------|
| Andi  S | Laki-laki | 14611155 |       |
| Iva     | Perempuan | 14611156 | 74.0  |
| Ihsan   | Laki-laki | 14611157 | 75.0  |
| Dewi    | Perempuan | 14611158 | 76.0  |
| Kurnia  | Perempuan | 14611159 | 39.0  |
| Eko     | Laki-laki | 14611160 | 65.0  |
| Tika    | Perempuan | 14611161 | 73.0  |
| Fitri   | Perempuan | 14611162 | 60.0  |
| Gita    | Perempuan | 14611163 | 63.0  |
| Hafidz  | Laki-laki | 14611164 | 75.0  |
| Maya    | Perempuan | 14611165 | 69.0  |
| Lukman  | Laki-laki | 14611166 | 75.0  |
| April   | Perempuan | 14611167 | 90.0  |
| Eka     | Perempuan | 14611168 | 84.0  |
| Wati    | Perempuan | 14611169 | 76.0  |

Didapatkan tabel baru yang terdiri dari ```Nama```, ```Kelamin```, ```NIM``` dan ```Nilai``` hasil penggabungkan kedua sheet sebelumnya. 