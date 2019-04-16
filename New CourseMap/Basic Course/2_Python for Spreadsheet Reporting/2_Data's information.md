# 02 Data's information

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada video kali ini kita akan menggali informsi dari data yang kita inputkan sebelumnya. 
```
data.info() 
```
*Output :* <br>
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 15 entries, 0 to 14
Data columns (total 3 columns):
Nama       15 non-null object
Kelamin    15 non-null object
Nilai      15 non-null int64
dtypes: int64(1), object(2)
memory usage: 440.0+ bytes
None
```
Didapatkan informasi bahwa terdapat baris 15 data dengan 3 kolom yaitu ```Nama```, ```Kelamin``` dan ```Nilai``` yang masing-masing mempunyai data lengkapatau tidak ada data kosong dan tipe data yang dimiliki ```Nama```, ```Kelamin``` bertipe object dan Nilai bertipe integer. 

Kemudian, kita dapat melihat data secara statistik dengan perintah
```
data.describe()
```
*Output :* <br>
|       | Nilai            |
|-------|------------------|
| count | 15.0             |
| mean  | 71.6             |
| std   | 11.8490505948789 |
| min   | 39.0             |
| 25%   | 67.0             |
| 50%   | 75.0             |
| 75%   | 76.0             |
| max   | 90.0             |

Dapat dilihat dari tabel diatas merupakan analisis deskriptif dari data yang kita inputkan. Pada fungsi ```.describe``` hanya menapilkan data yang berbentuk integer dan float. 

Mari kita mengurutkan data berdasarkan ```Nama``` dan index.
```
data = data.sort_values('Nama')
data = data.reset_index(drop=True)
data.head()
```
*Output :* <br>
|    | Nama   | Kelamin   | Nilai |
|----|--------|-----------|-------|
| 0  | Andi   | Laki-laki | 80    |
| 1  | April  | Perempuan | 90    |
| 2  | Dewi   | Perempuan | 76    |
| 3  | Eka    | Perempuan | 84    |
| 4  | Eko    | Laki-laki | 65    |
| 5  | Fitri  | Perempuan | 60    |

Didapatkan bahwa data diurutkan dari abjad ```Nama```. 

Selanjutnya kita akan mengurutkan sesuai nilai tertinggi sampai terendah
```
data = data.sort_values("Nilai", ascending=False)
data = data.reset_index(drop=True)
data.head()
```
*Output :* <br>
|    | Nama   | Kelamin   | Nilai |
|----|--------|-----------|-------|
| 0  | April  | Perempuan | 90    |
| 1  | Eka    | Perempuan | 84    |
| 2  | Andi   | Laki-laki | 80    |
| 3  | Dewi   | Perempuan | 76    |
| 4  | Wati   | Perempuan | 76    |
| 5  | Hafidz | Laki-laki | 75    |

Data telah terurut dari nilai tertinggi sampai terendah dengan nilai tertinggi 90 yaitu April. 