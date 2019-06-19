# Part 8

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Setelah kita mendefinisikan _feature_ dan _target_ dari data kita, serta mendefinisikan model yang akan kita gunakan pada video sebelumnya, sekarang kita akan menerapkan _Validation_ menggunakan _K-Fold Cross Validation_ untuk meninjau performa dari model kita.

Berikut adalah syntaxnya.

```
fold = int(input("How many Fold do you want?"))

kf = KFold(n_splits=fold, random_state=45)
kf.get_n_splits(X)
from sklearn.metrics import accuracy_score
print(kf)

# save our score
scoring = []
for train_index, test_index in kf.split(X):
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
