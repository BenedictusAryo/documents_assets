# 3-01 Multivariate Linear Regression

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah membahas tentang `single linear regression` yang menggunakan satu fitur. Nah, pada video kali ini kita akan membahas mengenai `linear regression` yang menggunakan banyak fitur. <br>
Nah, bagaimana sih caranya ? Caranya adalah sama seperti pada video sebelumnya yaitu kita harus mendefinisikan **X** dan **y** terlebih dahulu. Yang membedakan ialah nilai X pada kasus kali ini tidak satu melainkan semua variabel yang kita gunakan kecuali target. Perhatikan syntax berikut:

```
X = data_lin.drop('MEDV', axis = 1)
y = data_lin['MEDV]
```

Selanjutnya yaitu kita peru me-load model serta membagi datanya kedalam data train dan test menggunakan perintah berikut:

```
clf = LinearRegression()

X_train, X_test, y_train, y_test = train_test_split(X,y, test_size = 0.2, random_state=45)

clf.fit(X_train, y_train)
```

Jika data telah dibagi kedalam data train dan data test serta telah dilakukan fitting, kita dapat mengecek hasil fitting menggunakan perintah berikut:

```
clf.coef_
clf.intercept_
```
Hasil perintah diatas mengeluarkan output rumus regresi sebagai berikut :

$MEDV = -114.46564*CRIM + 48.10036*ZN + (-29.3283702 * INDUS) + 2331.53463 * CHAS + NOX + RM + AGE + DIS + RAD + TAX + PTRATIO + B + LSTAT$

Berdasarkan rumus diatas kita dapat melihat impact nya ke data testing lho menggunakan syntax berikut:
```
pred_2 = clf.predict(X_test)
pd.DataFrame ({'actual':y_test, 'pred_1':pred, 'pred_2':pred_2})
```

Nah, teman-teman sudah paham belum nih sampai sini? Kalau belum yuk simak semua penjelasan di video berikut.
