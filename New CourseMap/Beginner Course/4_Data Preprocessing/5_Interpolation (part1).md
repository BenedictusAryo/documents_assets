# 04 Interpolation 1

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Interpolasi merupakan mengisi nilai yang kosong dengan pola-pola tertentu biasa dengan data time series ( data yang berkaitan dengan waktu). 

```
data1 = pd.read_csv('http://bit.ly/machine_temperature')
data1.head()
``` 

*Output :*

| Measurement date | Machine temperature |
|------------------|---------------------|
| 20161227         | 46                  |
| 20161228         | 47                  |
| 20161229         | 48                  |
| 20161230         | 45                  |
| 20161231         | 47                  |

Pada data diatas terdiri dari dua variabel yaitu Measurement date dan Machine temperature. Mari kita cek terlebih dahulu apakah ada nilai yang kosong atau tidak dengan perintah

```
pd.isnull(data1).sum()
```

*Output :*

```
Measurement date       0
Machine temperature    0
dtype: int64
```

Data diatas tidak ada data yang kosong. Tetapi bila diperhatika lebih lanjut beberapa data terlangkah pada beberapa tanggal (beberapa tanggal tidak ada atau kosong). Nah, diperlukan untuk melengkapi data tersebut dengan mengubahnya dalam bentuk date time. 

```
data1['Measurement date'] = pd.to_datetime(data1['Measurement date'], format='%Y%m%d')
data1.head()
```

*Output :*

| Measurement date | Machine temperature |
|------------------|---------------------|
| 2016-12-27       | 46                  |
| 2016-12-28       | 47                  |
| 2016-12-29       | 48                  |
| 2016-12-30       | 45                  |
| 2016-12-31       | 47                  |

Pada tabel diatas Measurement date telah berubah ke format tahun-bulan-tanggal. Sebelum kita mengisi tanggal-tanggal yang kosong, kita akan mengubah index data menjadi Measurement date dengan perintah berikut

```
data1.set_index('Measurement date', inplace=True)
data1.head()
```
*Output :*

| Measurement date| Machine Temperature |
|-----------------|---------------------|
| 2016-12-27      | 46.0                |
| 2016-12-28      | 47.0                |
| 2016-12-29      | 48.0                |
| 2016-12-30      | 45.0                |
| 2016-12-31      | 47.0                |

Dari tabel diatas Measurement date menjadi sebuah index tidak lagi menjadi sebuah variabel. Tetapi tanggal yang tidak ada belum muncul maka digunakan perintah

```
allday = pd.date_range(data1.index.min(), data1.index.max(), freq='D')
data1 = data1.loc[allday]
data1.head(10)
```
*Output :*

|            | Machine Temperature |
|------------|---------------------|
| 2016-12-27 | 46.0                |
| 2016-12-28 | 47.0                |
| 2016-12-29 | 48.0                |
| 2016-12-30 | 45.0                |
| 2016-12-31 | 47.0                |
| 2017-01-01 | NaN                 |
| 2017-01-02 | 54.0                |
| 2017-01-03 | 52.0                |
| 2017-01-04 | NaN                 |
| 2017-01-05 | 47.0                |

Dapat dilihat bahwa nilai nilai yang kosong telah berbentuk NaN. 