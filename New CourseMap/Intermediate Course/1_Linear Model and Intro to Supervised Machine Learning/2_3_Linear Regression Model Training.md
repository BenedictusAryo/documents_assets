# 2-03 Linear Regression Model Training

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mempelajari bagaimana membagi data yang dipunyai ke dalam data training dan data testing. Nah, pada video kali ini kita akan mempelajari bagaimana caranya `mem-fitting model` berdasarkan data tersebut. 

Dalam melakukan fitting itu digunakan data training. Dimana dalam hal ini perbandingan untuk data training dan testing ialah 80% dan 20%. Oleh sebab itu pada kasus kali ini kita melakukan fitting pada data training menggunakan syntax :

```
clf.fit(x_train, y_train)
clf.coef_
clf.intercept_
pred = clf.predict(x_test)
```
Kemudian, berdasarkan hasil yang dipuyai lalu dilakukan perbandingan menggunakan `DataFrame` menggunakan syntax berikut:

```
pd.DataFrame({'actual':y_test,'prediction':pred})
```

Selengkapnya, yuk coba simak penjelasan pada video berikut ini.
