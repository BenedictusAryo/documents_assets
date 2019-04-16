# 11 Merging with VLOOKUP in Data Science 3

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Workbook Jupyter Notebook dan Dataset untuk bab ini bisa didownload di :[Exercise_Python for Spreadsheet.zip](https://drive.google.com/file/d/1WlpXDBTwluGYoV0crZ4fBtXglicXtS-A/view?usp=sharing)_

Pada video ini akan menggabungkan data dengan isi yang sama tetapi nama variabel yang berbeda yaitu pada variabel ```Nama``` pada sheet ```Kelamin``` dan ```Nama Sisawa``` pada sheet ```Nilai```. Mari kita inputkan dan melihat data pada sheet ```Kelamin``` dan ```Nilai```
```
data_workbook = pd.ExcelFile('data/data_nilai_matematika2.xlsx')
data_kelamin = data_workbook.parse('Kelamin')
data_kelamin.head()
```
*Output :*

| Nama   | Kelamin   |
|--------|-----------|
| Andi   | Laki-laki |
| Iva    | Perempuan |
| Ihsan  | Laki-laki |
| Dewi   | Perempuan |
| Kurnia | Perempuan |
```
data_nilai = data_workbook.parse('Nilai')
data_nilai.head()
```
*Output :*

| Nama Siswa | Nilai |
|------------|-------|
| Andi       | 80    |
| Iva        | 74    |
| Ihsan      | 75    |
| Dewi       | 76    |
| Kurnia     | 39    |

Nah, dari kedua sheet tersebut kita gabungkan dengan perintah
```
data_gabung = data_kelamin.merge(data_nilai, 
                   left_on='Nama', 
                   right_on='Nama Siswa', 
                   how='left')
data_gabung.head()
```
*Output :*

| Nama   | Kelamin   | Nama Siswa | Nilai |
|--------|-----------|------------|-------|
| Andi   | Laki-laki | Andi       | 80    |
| Iva    | Perempuan | Iva        | 74    |
| Ihsan  | Laki-laki | Ihsan      | 75    |
| Dewi   | Perempuan | Dewi       | 76    |
| Kurnia | Perempuan | Kurnia     | 39    |

Pada tabel diatas telah digabungkan antara Sheet ```Kelamin``` dan ```Nilai```. Karena Nama mahasiswa double maka lebih baik kita hapus salah satunya. Nah, disini kita hapus ```Nama Siswa``` dengan perintah
```
data_gabung.drop('Nama Siswa', axis=1)
```
*Output :*

| Nama   | Kelamin   | Nilai |
|--------|-----------|-------|
| Andi   | Laki-laki | 80    |
| Iva    | Perempuan | 74    |
| Ihsan  | Laki-laki | 75    |
| Dewi   | Perempuan | 76    |
| Kurnia | Perempuan | 39    |