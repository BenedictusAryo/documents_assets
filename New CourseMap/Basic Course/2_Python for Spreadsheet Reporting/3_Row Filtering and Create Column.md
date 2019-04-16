# 03 Row Filtering and Create Column

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada video kali ini membahas tentang menampilkan data-data yang kita perlukan. 

Kali ini kita akan melihat data hanya variabel ```Nama```
```
data[['Nama']]
```
*Output :*

|    | Nama   |
|----|--------|
| 0  | April  |
| 1  | Eka    |
| 2  | Andi   |
| 3  | Dewi   |
| 4  | Wati   |
| 5  | Hafidz |
| 6  | Ihsan  |
| 7  | Lukman |
| 8  | Iva    |
| 9  | Tika   |
| 10 | Maya   |
| 11 | Eko    |
| 12 | Gita   |
| 13 | Fitri  |
| 14 | Kurnia |

Kita akan melihat data untuk ```Gita```
```
data[data['Nama']=="Gita"]
```
*Output :*

|    | Nama | Kelamin   | Nilai |
|----|------|-----------|-------|
| 12 | Gita | Perempuan | 63    |

Dari tabel didapatkan bahwa gita berjenis kelamin perempuan dan mendapatkan nilai 63.

Selain itu, kita bisa mendapatkan nilai misalnya nilainya < 80.
```
data[data['Nilai']<80].reset_indes(drop=True)
```
*Output :*

|    | Nama   | Kelamin   | Nilai |
|----|--------|-----------|-------|
| 0  | Dewi   | Perempuan | 76    |
| 1  | Wati   | Perempuan | 76    |
| 2  | Hafidz | Laki-laki | 75    |
| 3  | Ihsan  | Laki-laki | 75    |
| 4  | Lukman | Laki-laki | 75    |
| 5  | Iva    | Perempuan | 74    |
| 6  | Tika   | Perempuan | 73    |
| 7  | Maya   | Perempuan | 69    |
| 8  | Eko    | Laki-laki | 65    |
| 9  | Gita   | Perempuan | 63    |
| 10 | Fitri  | Perempuan | 60    |
| 11 | Kurnia | Perempuan | 39    |

Tabel diatas telah didapatkan siapa saja yang mendapatkan nilai dibawah 80. 

