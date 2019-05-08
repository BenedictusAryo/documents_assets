# 06 Using Scikit-learn Package

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video sebelumnya, kita menghitung secara manual untuk mendapatkan formula model. Nah, kali ini kita akan mempelajari dengan menggunakan package sklearn dengan perintah

```
from sklearn.linear_model import LinearRegression
reg = LinearRegression()
x = dt[['Height']]
y = dt['Weight']
```

Selanjutnya, kita fitting data kedalam model 

```
reg.fit(x,y)
```

Mari kita periksa nilai nilai slope dan intercept. <br>
Untuk mengecek hasil slope kita gunakan `reg.coef_`
```
reg.coef_
```

*Output :* 

>array([1.42857143])


Kemudian kita gunakan `reg.intercept_` untuk mengetahui hasil interceptnya

```
reg.intercept_
```

*Output :* 


> -177.85714285714292


Kemudian, kita bentuk formula model
```
print('Weight =', reg.coef_[0], '* Height +',reg_intercept_)
```
*Output :* 

>Weight = 1.428571428571429 * Height + -177.85714285714292

Pada hasil pada output diatas formula model yang didapat sama dengan formula model yang kita hitung manual sebelumnya. Jadi, ketika kita fitting/training pada package sklearn maka pacakage tersebut akan menjalankan fungsi dari rumus di video sebelumnya. 