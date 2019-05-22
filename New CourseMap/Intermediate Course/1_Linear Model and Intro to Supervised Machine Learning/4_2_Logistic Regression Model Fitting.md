# 4-02 Logistic Regression Model Fitting

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, video kali ini kita akan melanjutkan materi pada video sebelumnya. Dimana selanjutnya yaitu kita memanggil fungsi regression pada python seperti berikut:

```
clf = LogisticRegression() 
```

Nah, selanjutnya kita membagi nilai X dan y nya. Dimana dalam hal ini X nya ialah variabel `balance` dan nilai y nya ialah variabel `default`.

```
X = data_log[['balance']]
y = data_log['default']

X_train, X_test, y_train, y_test = train_test_split(X,y, test_size = 0.2, random_state=45)

clf.fit(X_train, y_train)
```

Kemudian, kita bisa memasukkan fungsi regression, sebagai berikut:

```
clf.coef_
clf.intercept_
```

Nah, untuk lebih jelasnya yuk kita simak video berikut.

