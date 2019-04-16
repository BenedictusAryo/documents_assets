# 04 Create New Columns

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada video kali ini akan ditambahkan kolom baru. 

Kali ini kita akan menambahkan kolom baru dengan nama ```Kolom_akhir``` dengan fungsi ```Nilai```+10.
```
data['Nilai_akhir'] = data['Nilai']+10
data.head()
```
*Output :*

|    | Nama   | Kelamin   | Nilai | Nilai_akhir |
|----|--------|-----------|-------|-------------|
| 0  | April  | Perempuan | 90    | 100         |
| 1  | Eka    | Perempuan | 84    | 94          |
| 2  | Andi   | Laki-laki | 80    | 90          |
| 3  | Dewi   | Perempuan | 76    | 86          |
| 4  | Wati   | Perempuan | 76    | 86          |
| 5  | Hafidz | Laki-laki | 75    | 85          |

Data baru akan diinputkan ditabel data yang kita punya. Data yang akan diinputkan yaitu dengan nama Didi, Jenis Kelamin Laki-laki, Nilai 90 dengan perintah
```
data1 = [{'Nama' : "Didi", 'Kelamin' : "Laki-laki", 'Nilai' : 89, 'Nilai_akhir' : 89+10}]
baru1 = pd.DataFrame(data1)
data = data.append(baru1).reset_index(drop=True)
data.tail()
```
*Output :*

|    | Kelamin   | Nama   | Nilai | Nilai_akhir |
|----|-----------|--------|-------|-------------|
| 10 | Perempuan | Maya   | 69    | 79          |
| 11 | Laki-laki | Eko    | 65    | 75          |
| 12 | Perempuan | Gita   | 63    | 73          |
| 13 | Perempuan | Fitri  | 60    | 70          |
| 14 | Perempuan | Kurnia | 39    | 49          |
| 15 | Laki-laki | Didi   | 89    | 99          |

Maka data baru yang kita masukkan akan bergabung dengan data yang kita inputkan sebelumnya. 