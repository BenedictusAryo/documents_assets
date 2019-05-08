# 08 MSE Calculation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan menghitung MSE (Mean Squared Error) dari analisis yang telah kita lakukan sebelumnya. Sebelumnya kita perlu mencari nilai prediksi terlebih dahulu dengan perintah

```
weight_pred = reg.predict(x)
hasil = pd.DataFrame({'Weight':y,
                     'Weight_Prediction':weight_pred})
hasil
```

*Output :* 

| Weight | Weight_Prediction  |
|--------|--------------------|
| 40     | 36.428571428571445 |
| 50     | 50.71428571428572  |
| 60     | 65.00000000000003  |
| 65     | 72.14285714285717  |
| 55     | 57.85714285714286  |
| 45     | 43.571428571428584 |
| 90     | 79.2857142857143   |

Pada tabel diatas merupakan data sebenarnya dan data prediksi dari analisis yang telah kita lakukan. Nah selanjutnya mari kita mencari nilai error dengan perintah

```
hasil['Error'] = hasil['Weight'] - hasil['Weight_Prediction']
hasil
```

*Output :* 

| Weight | Weight_Prediction  | Error               |
|--------|--------------------|---------------------|
| 40     | 36.428571428571445 | 3.571428571428555   |
| 50     | 50.71428571428572  | -0.7142857142857224 |
| 60     | 65.00000000000003  | -5.000000000000028  |
| 65     | 72.14285714285717  | -7.142857142857167  |
| 55     | 57.85714285714286  | -2.857142857142861  |
| 45     | 43.571428571428584 | 1.4285714285714164  |
| 90     | 79.2857142857143   | 10.714285714285694  |

Setelah didapatkan nilai error, maka kita dapat menghitung MSE dengan perintah 

```
(hasil ['Error']**2).mean()
```

*Output :* 

>30.612244897959194

Pada MSE diatas dihitung secara manual. Nah, sekarang kita gunakan package dengan perintah

```
from sklearn.metrics impot mean_squared_error
mean_square_error(weight_pred, y)
```

*Output :* 

>30.612244897959194

Maka didapatkan hasilyang sama dengan perhitungan manual. 