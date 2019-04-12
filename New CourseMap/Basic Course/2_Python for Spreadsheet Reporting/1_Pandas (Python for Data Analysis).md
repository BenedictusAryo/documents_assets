# 02 Pandas

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pembelajaran kali ini akan membahas tentang "python for spreadsheet" yaitu mempelajari python yang biasanya kita pelajari di speadsheet. Sebelumnya, ada salah satu package yang akan membantu kita mengproses lebih lanjut yaitu package pandas yang merupakan sebuah package sebagai alat analisis terstruktur untuk bahasa pemrograman python. Salah satu kegunaan pandas yaitu mengubah data kita menjadi dataframe. 
```
import pandas as pd
```
Pada pembahasan ini kita menggunakan kasus data nilai matematika. 
```
data = pd.read_excel('data/data_nilai_matematika.xlsx')
print(data)
```
*Output :* <br>
| Nama   | Kelamin   | Nilai |
|--------|-----------|-------|
| Andi   | Laki-laki | 80    |
| Iva    | Perempuan | 74    |
| Ihsan  | Laki-laki | 75    |
| Dewi   | Perempuan | 76    |
| Kurnia | Perempuan | 39    |
| Eko    | Laki-laki | 65    |
| Tika   | Perempuan | 73    |
| Fitri  | Perempuan | 60    |
| Gita   | Perempuan | 63    |
| Hafidz | Laki-laki | 75    |
| Maya   | Perempuan | 69    |
| Lukman | Laki-laki | 75    |
| April  | Perempuan | 90    |
| Eka    | Perempuan | 84    |
| Wati   | Perempuan | 76    |

Dari data diatas kita ketahui bahwa data terdiri dari Nama, Kelamin dan Nilai. Misalnya kita ingin melihat 5 data awal
```
data.head()
```
*Output :* <br>
| Nama   | Kelamin   | Nilai |
|--------|-----------|-------|
| Andi   | Laki-laki | 80    |
| Iva    | Perempuan | 74    |
| Ihsan  | Laki-laki | 75    |
| Dewi   | Perempuan | 76    |
| Kurnia | Perempuan | 39    |

Sekarang kita lihat 2 data teratas
```
data.head(2)
```
*Output :* <br>
| Nama   | Kelamin   | Nilai |
|--------|-----------|-------|
| Andi   | Laki-laki | 80    |
| Iva    | Perempuan | 74    |

Memilihi perbedaan ketika kita ingin melihat data ketiga sampai kedelapan
```
data[3:9]
```
*Output :* <br>
| Nama   | Kelamin   | Nilai |
|--------|-----------|-------|
| Dewi   | Perempuan | 76    |
| Kurnia | Perempuan | 39    |
| Eko    | Laki-laki | 65    |
| Tika   | Perempuan | 73    |
| Fitri  | Perempuan | 60    |
| Gita   | Perempuan | 63    |