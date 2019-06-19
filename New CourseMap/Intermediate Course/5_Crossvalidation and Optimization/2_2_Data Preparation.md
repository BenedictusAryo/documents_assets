# 2_2_Data Preparation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini, kita akan melanjutkan praktek dalam mengimplementasikan _validation_ dan _optimization_ pada model yang akan kita buat.

Dataset dapat di download pada link berikut : <br>
> [diabetes.csv](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AAC4umEKNsycG0ibVwQ4SQ4ga/diabetes.csv?dl=0)

Setelah kita melakukan _import packages_, kita akan mendefinisikan _feature_(X) dan _target_(y) dari data kita. Berikut adalah syntaxnya.

```
X = data.drop('Outcomes', axis = 1)
y = data ['Outcomes']
```

Lalu selanjutnya kita memastikan bahwa yang kita ambil adalah _value_ dari datanya saja yang bertipe data numpy array.

```
X = X.values
y = y.values
```

Setelah data sudah didefinisikan, kita mulai mendefinisikan model kita. Dalam contoh kali ini kita akan menggunakan _DecisionTreeClassifier_. Selain itu kita juga mendefinisikan beberapa parameter yang terdapat pada model kita.

```
model_dt = DecisionTreeClassifier(criterion = 'entropy')
```
