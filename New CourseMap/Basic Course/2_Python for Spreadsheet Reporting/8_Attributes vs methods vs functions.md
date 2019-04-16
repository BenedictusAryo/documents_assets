# 08 Attributes vs methods vs functions

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada pembahasan video kali ini kita akan membahasa perbedaan **Attributes, methods** dan **Functions**. 

Kita akan tampilkan data sheet ```Kelamin``` dan ```Nilai```
```
data_kelamin = data_workbook.parse('Kelamin')
data_kelamin.head()
```
*Output :*

| Nama    | Kelamin   | NIM      |
|---------|-----------|----------|
| ANDI  S | Laki-laki | 14611155 |
| IVA     | Perempuan | 14611156 |
| IHSAN   | Laki-laki | 14611157 |
| DEWI    | Perempuan | 14611158 |
| KURNIA  | Perempuan | 14611159 |
```
data_nilai = data_workbook.parse('Nilai')
data_nilai.head()
```
*Output :*

| Nama   | Nilai |
|--------|-------|
| Andi S | 80    |
| Iva    | 74    |
| Ihsan  | 75    |
| Dewi   | 76    |
| Kurnia | 39    |

Dari penginputan data diatas bisa kita ketahui sebagai berikut:
```
pd.ExcelFile() (function)
workbook.sheet_names (attribute)
workbook.parse() (method)
```