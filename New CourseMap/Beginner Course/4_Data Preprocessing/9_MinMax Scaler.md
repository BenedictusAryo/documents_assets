# 08 MinMax Scaler

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Numerical Data Normalization merupakan proses normalisasi data dengan bentuk numerik. Data berbentuk numerik sebelumnya harus kita pilih terlebih dahulu. Perlu diperhatikan data numerik dengan data kategorik, karena keduanya mempunyai metode normalisasi yang berbeda. 

Pada pembahasan kali ini membahasa Min Max Scaler merupakan proses normalisasi data supaya mendapatkan output nilai dari 0 sampai 1 untuk data numerik. Pada kasus data kita data numerik yang digunakan yaitu ```Age```, ```SibSp```, ```Parch``` dan ```Fare```.

```
from sklearn.preprocessing import MinMaxScaler
scaler1 = MinMaxScaler()
data_num = df1[['Age', 'SibSp', 'Parch', 'Fare']]
data_m = scaler1.fit_transform(data_num)
data_m
```

*Output :*

```
array([[0.27117366, 0.125     , 0.        , 0.01415106],
       [0.4722292 , 0.125     , 0.        , 0.13913574],
       [0.32143755, 0.        , 0.        , 0.01546857],
       ...,
       [0.34656949, 0.125     , 0.33333333, 0.04577135],
       [0.32143755, 0.        , 0.        , 0.0585561 ],
       [0.39683338, 0.        , 0.        , 0.01512699]])
```

Dari output diatas data numerik telah ternormalisasi. Tetapi permasalahan saat ini, kita akan susah melihat arti dari data tersebut. Maka diperlukan dataframe untuk membentuk tampilan lebih baik dengan perintah

```
data_m = pd.DataFrame(data_m, columns = ['Age','SibSp', 'Parch', 'Fare'])
data_m.head()
```

*Output :*

| Age                 | SibSp | Parch | Fare                 |
|---------------------|-------|-------|----------------------|
| 0.2711736617240512  | 0.125 | 0.0   | 0.014151057562208049 |
| 0.4722292033174164  | 0.125 | 0.0   | 0.13913573538264068  |
| 0.32143754712239253 | 0.0   | 0.0   | 0.015468569817999833 |
| 0.4345312892686604  | 0.125 | 0.0   | 0.10364429745562033  |
| 0.4345312892686604  | 0.0   | 0.0   | 0.015712553569072387 |

Pada tabel diatas merupakan hasil normalisasi setiap kolom. Hasil dari tabel diatas lebih mudah untuk melihat arti dari data. 