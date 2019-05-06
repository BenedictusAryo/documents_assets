# 05 Interpolation 2

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pembelajaran kali ini kita akan mempelajarai interpolasi yang cukup general yang dipakai yaitu Nearest dan Linear. 

Mari kita coba untuk metode linear
```
data_near = data1.interpolate(method='linear')
data_near.head(10)
```

*Output :*

|            | Machine Temperature |
|------------|---------------------|
| 2016-12-27 | 46.0                |
| 2016-12-28 | 47.0                |
| 2016-12-29 | 48.0                |
| 2016-12-30 | 45.0                |
| 2016-12-31 | 47.0                |
| 2017-01-01 | 50.5                |
| 2017-01-02 | 54.0                |
| 2017-01-03 | 52.0                |
| 2017-01-04 | 49.5                |
| 2017-01-05 | 47.0                |

Pada tabel diatas dari nilai yang kosong telah diisi dengan suatu nilai desimal. Diperlukan visualisasi untuk melihat pola data 
```
data_near.resample('D').mean().plot();
```
*Output :* 

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/4_Data%20Preprocessing/Assets/Figure_1.png" width="360" height="260" align="center"/>

Pada gambar diatas dapat dilihat misalnya pada tangal 2017-01-10 sampai 2017-10-16 yaitu data yang kosong, maka di garfik tersebut akan membentuk garis linier penghubung dari data sebelumnya dan sesudahnya.

Lalu mari kita coba untuk metode Nearest

```
data_est = data1.interpolate(method='nearest')
data_est.resample('D').mean().plot();
```

*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/4_Data%20Preprocessing/Assets/Figure_1-1.png" width="360" height="260" align="center"/>

Jika dibandingkan dengan metode linier, metode nearest mempunyai format yang berbeda. 