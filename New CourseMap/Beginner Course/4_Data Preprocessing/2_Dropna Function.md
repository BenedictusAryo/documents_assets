# 02 Dropna Function

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pembelajaran kali ini membahasa ```dropna function``` yaitu menghapus semua data yang terdapat nilai kosong. 

Pertama kita meng-copy data df ke dalam df1, yang berfungsi sebagai agar data persis dengan data aslinya.

```
df1 = df.copy()
df1.shape
```
*Output :*

(891, 12)

Pada output diatas data diketahui mempunyai 891 baris dan 12 kolom. Tetapi ketika nilai kosong semua data yang terdapat nilai kosong dihapus maka akan didapat kan hasil dengan perintah
```
df1.dropna().shape
```
*Output :*

(183, 12)

Didapatkan 183 baris dan 12 kolom. Selain itu, kita dapat menghapus kolom terterntu. Pada kasus ini kita akan menghapus kolom Cabin dan Name dengan perintah
```
df1.drop(['Cabin', 'Name'], axis=1)
```
*Output :*

| PassengerId | Survived | Pclass | Sex    | Age  | SibSp | Parch | Ticket           | Fare    | Embarked |
|-------------|----------|--------|--------|------|-------|-------|------------------|---------|----------|
| 1           | 0        | 3      | male   | 22.0 | 1     | 0     | A/5 21171        | 7.25    | S        |
| 2           | 1        | 1      | female | 38.0 | 1     | 0     | PC 17599         | 71.2833 | C        |
| 3           | 1        | 3      | female | 26.0 | 0     | 0     | STON/O2. 3101282 | 7.925   | S        |
| 4           | 1        | 1      | female | 35.0 | 1     | 0     | 113803           | 53.1    | S        |
| 5           | 0        | 3      | male   | 35.0 | 0     | 0     | 373450           | 8.05    | S        |