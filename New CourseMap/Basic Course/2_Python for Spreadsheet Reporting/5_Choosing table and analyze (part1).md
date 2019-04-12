# 05 Choosing table and analyze 1

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pembahasan kali ini kita akan memilih tabel dan menganalisanya secara statistik. 

Pada kasus ini akan membahas tentang data penjualan motor tahun 2018. 
```
import pandas as pd
motor = pd.read_excel('data/data_penjualan_motor2018.xlsx')
motor.head()
```
*Output :* <br>
| Bulan     | Jenis    | Jumlah |
|-----------|----------|--------|
| Januari   | Honda    | 345957 |
| Februari  | Honda    | 339152 |
| Maret     | Honda    | 384187 |
| April     | Honda    | 458499 |
| Mei       | Honda    | 436727 |

Data yang kita punya mempunyai variabel ```Bulan```, ```Jenis``` dan ```Jumlah```. 

Kita jumlahkan data penjualan tahun 2018 dengan perintah
```
motor.sum(numeric_only=True)
```
*Output :* <br>
```
Jumlah    6382780
dtype: int64
```
Jumlah yang didapatkan yaitu sebanyak 6382780. Ketika kita hendak mengetahui penjualan perbulan dengan perintah
```
motor.groupby('Bulan', as_index=False).sum()
```
*Output :* <br>
| Bulan     | Jumlah |
|-----------|--------|
| Agustus   | 567961 |
| April     | 580917 |
| Desember  | 453162 |
| Februari  | 439537 |
| Januari   | 136549 |
| Januari   | 345957 |
| Juli      | 593728 |
| Juni      | 375015 |
| Maret     | 535359 |
| Mei       | 589286 |
| November  | 597347 |
| Oktober   | 610295 |
| September | 557667 |

Selanjutnya, untuk memudahkan pemahaman kita akan mencari menurut bulan dan jenisnya.
```
motor.groupby(['Bulan','Jenis'], as_index=False).sum()
```
*Output :* <br>
| Bulan     | Jenis    | Jumlah |
|-----------|----------|--------|
| Agustus   | Honda    | 443694 |
| Agustus   | Kawasaki | 7016   |
| Agustus   | Suzuki   | 8355   |
| Agustus   | Yamaha   | 108896 |
| April     | Honda    | 458499 |

Nah, kali ini kita mencari data bulan Januari dan jenis Yamaha
```
motor[(motor['Jenis'] == 'Yamaha') & (motor['Bulan']=='Januari')]
```
*Output :* <br>
| Bulan     | Jenis    | Jumlah |
|-----------|----------|--------|
| Januari   | Yamaha   | 122989 |

Didapatkan jumlah motor yang terjual pada bulan januari dengan jenis yamaha sebanyak 122989. 