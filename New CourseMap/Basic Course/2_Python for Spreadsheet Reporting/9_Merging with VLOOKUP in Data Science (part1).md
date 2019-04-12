# 09 Merging with VLOOKUP in Data Science (How to Handle Case Sensitive)

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Sebelumnya, perlu diketahui bahwa Python merupakan program yang case-sensitive (sensitive terhadap perbedaan. misalnya: huruf besar dengan huruf kecil, spasi, dll). Nah, kita bisa meng-handle data kita yang mempunyai isi variabel yang sama.

Mengubah data dengan semua huruf kecil.
```
data_kelamin['Nama'] = data_kelamin['Nama'].str.lower()
data_kelamin.head()
```
*Output :* <br>
| Nama    | Kelamin   | NIM      |
|---------|-----------|----------|
| andi  s | Laki-laki | 14611155 |
| iva     | Perempuan | 14611156 |
| ihsan   | Laki-laki | 14611157 |
| dewi    | Perempuan | 14611158 |
| kurnia  | Perempuan | 14611159 |

Mengubah data dengan semua huruf besar
```
data_kelamin['Nama'] = data_kelamin['Nama'].str.upper()
data_kelamin.head()
```
*Output :* <br>
| Nama    | Kelamin   | NIM      |
|---------|-----------|----------|
| ANDI  S | Laki-laki | 14611155 |
| IVA     | Perempuan | 14611156 |
| IHSAN   | Laki-laki | 14611157 |
| DEWI    | Perempuan | 14611158 |
| KURNIA  | Perempuan | 14611159 |

Mengubah data dengan semua huruf besar diawal kata
```
data_kelamin['Nama'] = data_kelamin['Nama'].str.title()
data_kelamin.head()
```
*Output :* <br>
| Nama    | Kelamin   | NIM      |
|---------|-----------|----------|
| Andi  S | Laki-laki | 14611155 |
| Iva     | Perempuan | 14611156 |
| Ihsan   | Laki-laki | 14611157 |
| Dewi    | Perempuan | 14611158 |
| Kurnia  | Perempuan | 14611159 |