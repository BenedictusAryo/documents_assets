# 07 Working with Multiple Sheets

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada pembahasan pada video ini kita akan dihdapatkan ketika mempunyai beberapa sheet. 

Pada kasus kali ini kita mempunyai 2 sheet yaitu sheet ```Kelamin``` dan sheet ```Nilai```. Mari kita inputkan terlebih dahulu data yang kita punya.
```
import pandas as pd
data_workbook = pd.ExcelFile('data/data_nilai_matematika1.xlsx')
data_workbook
```
*Output :* <br>
```
<pandas.io.excel.ExcelFile object at 0x000000000826D198>
```

Pada output diatas kita tidak bisa membentuk datanya karena mempunyai 2 sheet. Maka kita perlu menganalisa dengan sheet ```Kelamin``` atau ```Nilai```.

Kita dapat menampilkan datanya dengan menggunakan ```Atribut``` dengan perintah
```
data_sheet_names = data_workbook.sheet_names
print(data_sheet_names)
```
*Output :* <br>
['Kelamin', 'Nilai']

Didapatkanlah nama sheet yang kita punya seperti output diatas. 