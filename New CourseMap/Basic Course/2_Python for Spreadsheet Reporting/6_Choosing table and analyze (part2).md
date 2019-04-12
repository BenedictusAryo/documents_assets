# 06 Choosing table and analyze 2

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Melanjutkan video sebelumnya, kita akan melihat infomarmasi data dengan perintah
```
motor.info()
```
*Output :* <br>
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 48 entries, 0 to 47
Data columns (total 3 columns):
Bulan     48 non-null object
Jenis     48 non-null object
Jumlah    48 non-null int64
dtypes: int64(1), object(2)
memory usage: 1.2+ KB
```

data kita memiliki 48 baris dan 3 kolom yaitu Bulan Jenis dan Jumlah. Kemudian, kita dapat mencari rata-rata penjualan sesuai jenis motornya.
```
motor.groupby(['Jenis'], as_index=False).mean()
```
*Output :* <br>
| Jenis    | Jumlah             |
|----------|--------------------|
| Honda    | 396600.1666666667  |
| Kawasaki | 6581.833333333333  |
| Suzuki   | 7459.0             |
| Yamaha   | 121257.33333333333 |

Pengurutan penjualan sesuai Jenis dan Bulan 
```
totals = motor.sort_values('Jumlah', 
                           ascending=False).reset_index(drop=True)
totals.head()
```
*Output :* <br>
| Bulan     | Jenis    | Jumlah |
|-----------|----------|--------|
| April     | Honda    | 458499 |
| Oktober   | Honda    | 456582 |
| Juli      | Honda    | 450622 |
| Agustus   | Honda    | 443694 |
| November  | Honda    | 440659 |

Didapatkan bahwa Top 5 penjualan terbanyak yaitu Honda dengan bulan April  yang paling tinggi. 

Nah, mari kita filtering penjualan untuk jenis ```Yamaha```.
```
motor1 = motor[motor['Jenis'] == 'Yamaha'].reset_index(drop=True)
motor1
```
*Output :* <br>
| Bulan     | Jenis  | Jumlah |
|-----------|--------|--------|
| Januari   | Yamaha | 122989 |
| Februari  | Yamaha | 85429  |
| Maret     | Yamaha | 133126 |
| April     | Yamaha | 113182 |
| Mei       | Yamaha | 140068 |
| Juni      | Yamaha | 96150  |
| Juli      | Yamaha | 127101 |
| Agustus   | Yamaha | 108896 |
| September | Yamaha | 134419 |
| Oktober   | Yamaha | 138012 |
| November  | Yamaha | 140683 |
| Desember  | Yamaha | 115033 |

Membuat function untuk melihat Maximal, mean dan minimal data.
```
def get_stats(group):
    return {'min': group.min(), 'max': group.max(), 'mean': group.mean()}
groupby = motor['Jumlah'].groupby(motor['Jenis']).apply(get_stats).unstack()
groupby
```
*Output :* <br>
| Jenis    | max      | mean               | min      |
|----------|----------|--------------------|----------|
| Honda    | 458499.0 | 396600.1666666667  | 271206.0 |
| Kawasaki | 13969.0  | 6581.833333333333  | 2282.0   |
| Suzuki   | 10489.0  | 7459.0             | 4077.0   |
| Yamaha   | 140683.0 | 121257.33333333333 | 85429.0  |

Pada tabel diatas, pada Jenis motor Honda penjualan terbanyak dengan 458499 unit, dengan rata-rata penjualan 396600 unit dan penjualan terkecil 271206 unit, dan seterusnya bisa dilihat pada tabel diatas.