# 10 Label Encoder 1

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Kali ini kita akan membahas tentang categorical data normalization yang merupakan normalisasi untuk data kategorik. Nah untuk data kita data yang termasuk kedalam kategorik yaitu ```Pclass```, ```Sex``` dan ```Embarked```. 
```
data_cat = df[['Pclass','Sex','Embarked']]
data.cat.head()
```
*Output :*

| Pclass | Sex    | Embarked |
|--------|--------|----------|
| 3      | male   | S        |
| 1      | female | C        |
| 3      | female | S        |
| 1      | female | S        |
| 3      | male   | S        |

Dari tabel diatas dapat kita ketahui bahwa kita telah memisahkan data kategorik. 

Pada categorical data normalization yang akan kita bahas yaitu metode Label Encoder dan One Hot Encoder. Mari kita coba dengan menggunakan Label Encoder terlebih dahulu dengan contoh berikut
    data_raw  = [France, Belgium, Germany, France, Germany]

     data_norm = [0, 1, 2 ,0, 1]

```
from sklearn.preprocessing import LabelEncoder
encoder1 = LabelEncoder()
data_2=data_cat.copy()
encoder1.fit(data_2.iloc[:,1])
encoder1.classes_
```

*Output :* 

array(['female', 'male'], dtype=object)

Pada syntax ```encoder1.fit(data_2.iloc[:,1])``` menunjukkan akan memproses kolom tabel ke 2 yaitu ```Sex```. Dari output diatas merupakan urutan normalisasi variabel ```Sex``` dengan female dengan nilai 0 dan male dengan nilai 1. 