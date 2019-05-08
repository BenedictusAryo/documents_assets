# 09 MAE Calculation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pemahasan pada video ini akan mencari nilai MAE(Mean Absolute Error) dari analissi yang telah kita lakukan sebelumnya. Meneruskan dari perhitungan MSE pada video sebelumnya, kita mencari rata-rata error yang telah di absolutkan dengan perintah

```
hasil['Error'].abs().mean()
```

*Output :* 

>4.489795918367349

Kemudian, kita menghitung MAE dengan package dengan perintah

```
fom sklearn.metrics import mean_absolute_error
mean_absolute_error(weight_pred, y)
```

*Output :* 

>4.489795918367349

Didapatkan nilai yang sama dengan perhitungan manual diatas. 