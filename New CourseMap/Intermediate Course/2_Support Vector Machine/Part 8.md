# Part 8

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dilakukan light processing pada data yang dipunyai. Pada video kali ini kita akan  membahas bagaimana membuat model berdasarkan video sebelumnya. 

Untuk pembuatan modelnya ini data yang digunakan yaitu data dari variabel *sepal_length* dan *sepal_width*.
```
X = data[['sepal_length','sepal_width']]
y = data['new_species']
```
Kemudian, data yang dimiliki dilakukan pembagian berdasarkan data training dan data testing.
```
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.3, random_state = 45)
X_train
y_train
X_test
y_test
```
Nah, sampai sini udah paham? kalau belum, yuk simak penjelasan pada video berikut.