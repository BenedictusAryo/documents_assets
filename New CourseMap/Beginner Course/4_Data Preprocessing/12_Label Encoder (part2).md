# 11 Label Encoder 2

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Dari pembahasan pada video sebelumnya, nilai classes telah kita dapatkan yaitu female kemudian male. Kemudian kita akan mentransformasi data kategorik tersebut
```
a = encoder1.transform(data_2.iloc[:,1])
a = pd.DataFrame(a)
a.head()
```
*Output :* 

| 0 |
|---|
| 1 |
| 0 |
| 0 |
| 0 |
| 1 |

Maka dari tabel diatas kita telah berhasil menormalisasi nilai pada kolom ```Sex```. Untuk memudahkan kita normalisasi langsung semua kolom atau tidak satu persatu seperti pada proses diatas yaitu dengan menggunakan looping berikut

```
length = data_2.shape[1]
col = data_2.columns
for i in range (length):
    print(i)
    a = encoder1.fit_transform(data_2.iloc[:,i:i+1])
    a = pd.DataFrame(a, columns=[col[i]+'new'])
    data_2 = data_2.join(a)
```

*Output :* 

| Pclass | Sex    | Embarked | Pclassnew | Sexnew | Embarkednew |
|--------|--------|----------|-----------|--------|-------------|
| 3      | male   | S        | 2         | 1      | 2           |
| 1      | female | C        | 0         | 0      | 0           |
| 3      | female | S        | 2         | 0      | 2           |
| 1      | female | S        | 0         | 0      | 2           |
| 3      | male   | S        | 2         | 1      | 2           |

data pada tabel diatas merupakan data asli dari ```Pclass```, ```Sex``` dan ```Embarked``` kemudian disusul oleh data baru yang telah dinormalisasi dari setiap kolom dari data asli tersebut yaitu dengan nama ```Pclassnew```, ```Sexnew``` dan ```Embarkednew```. 