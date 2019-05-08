# 10 $R^2$ Calculation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Video kali ini kita akan mencari nilai R-square dari analisis yang telah kita lakukan. Dari rumus yang telah kita kita bahas pada video 7. Kali ini R-square tersebut akan kita hitung manual. Pertama kita mencari nilai SSpred dengan perintah

```
ss_pred = (hasil['Error']**2).sum()
ss_pred
```

*Output :* 

>214.28571428571436

Kemudian, kita cari nilai SSmean dengan perintah

```
avg = hasil['Weight'].mean()
hasil['Minus_mean'] = hasil['Weight'] - avg
ss_mean = (hasil['Minus_mean']**2).sum()
ss_mean
```

*Output :* 

>1642.857142857143

Nah, kita bisa menghitung nilai `R-square` dengan perintah

```
1-(ss_pred/ss_mean)
```

*Output :* 

>0.852173913043

Maka didapatkan nilai `R-square` sebesar __85.217%__ yang artinya mcukup baik. Selanjutnya, kitta akan mencoba dengan menggunakan package dengan perintah

```
from sklearn.metrics import r2_score
r2_score(weight_pred, y)
```

*Output :* 

>0.850000000000001

Maka nilainya cukup berbeda namun tidak signifikan. 