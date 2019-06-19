# 3_2_LOOCV Crossvalidation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya, kita telah mencoba menggunakan _K-Fold Cross Validation_ untuk meninjau performa dari model yang kita miliki. Pada video kali ini kita akan menerapkan _Validation_ menggunakan _Leave One Out Cross Validation_ untuk meninjau performa dari model kita.

Berikut adalah syntaxnya.

```
loo = LeaveOneOut()
loo.get_n_splits(X)

print(loo)
scoring = []
for train_index, test_index in loo.split(X):
    X_train, X_test = X[train_index], X[test_index]
    y_train, y_test = y[train_index], y[test_index]
    model_dt.fit(X_train,y_train)
    pred = model_dt.predict(X_test)
    hasil = accuracy_score(y_test, pred)
    print("Score in Decision Tree : ", hasil)
    scoring.append(hasil)
scoring = np.array(scoring)
print(scoring.mean())
```
