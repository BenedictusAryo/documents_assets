# 02 Dataframe Describe

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini, kita akan langsung mempraktekkan Data Explorasi yang pertama yakni ```describe```, function describe yang terdapat pada pandas ini dapat langsung kita panggil setelah mendefinisikan tabel dataframenya pada Jupyter notebook.

```
import pandas as pd

df = pd.read_csv('http://bit.ly/drinksbycountry')
df.describe()
```
*Output :*


|              |beer_servings    |spirit_servings|wine_servings|total_litres_of_pure_alcohol|
|--------------|----------------:|--------------:|------------:|---------------------------:|
|**count**     |193.000000       |193.000000     |193.000000   |                  193.000000|
|**mean**      |106.160622       | 80.994819     | 49.450777   |                    4.717098|
|**std**       |101.143103       | 88.284312     | 79.697598   |                    3.773298|
|**min**       |  0.000000       |  0.000000     |  0.000000   |                    0.000000|
|**25%**       | 20.000000       |  4.000000     |  1.000000   |                    1.300000|
|**50%**       | 76.000000       | 56.000000     |  8.000000   |                    4.200000|
|**75%**       |188.000000       |128.000000     | 59.000000   |                    7.200000|
|**max**       |376.000000       |438.000000     |370.000000   |                   14.400000|

Seperti yang terlihat, setelah memasukkan perintah ```df.describe()```, akan terlihat sebuah tabel baru yang berisi tentang informasi statistik deskriptif dari tabel ```df``` tersebut, seperti *count* yakni jumlah baris yang memiliki data pada tiap-tiap kolom, *mean* atau rata-rata, hingga nilai *interquartil* dari tiap-tiap kolom pada data ```df``` tersebut.

Selain itu, kita juga dapat melihat informasi tipe data dari tiap-tiap kolom yang ada pada tabel df dengan menggunakan ```df.info```.
```
df.info()
```
*Output :*
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 193 entries, 0 to 192
Data columns (total 6 columns):
country                         193 non-null object
beer_servings                   193 non-null int64
spirit_servings                 193 non-null int64
wine_servings                   193 non-null int64
total_litres_of_pure_alcohol    193 non-null float64
continent                       193 non-null object
dtypes: float64(1), int64(3), object(2)
memory usage: 9.1+ KB
```

Maka akan terlihat informasi seperti tipe data dari df sendiri, yakni ```<class 'pandas.core.frame.DataFrame'>``` karena kita tahu bahwa df merupakan sebuah dataframe. Kemudian kita melihat nilai **193** yakni jumlah baris data pada tiap kolom (terdapat 6 kolom) dan kemudian kita juga dapat mengetahui tipe data pada tiap-tiap kolomnya seperti *object* atau string yakni nama Negara dan nama Benua, serta nilai konsumsi minuman yang berjenis integer dan float jika memiliki nilai koma.