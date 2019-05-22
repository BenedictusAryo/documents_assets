# 4-03 Logistic Regression Predict Probability

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, selanjutnya bagaimana caranya kita menghitung agar bentuknya menjadi ke dalam bentuk `logistic regression`? Dalam hal ini kita perlu mengambil nilai output dari perhitungan yang telah dilakukan pada video sebelumnya menggunakan perintah berikut:

```
X_train.head()
0.00423834 * 334.466420 - 8.60235278
p = e^y / (e^y+1)
math.exp(-7.1847703734572) / (math.exp(-7.1847703734572)+1)
```

```
clf.predict_proba(X_train)
```
Nah, untuk penjelasan engkapnya bisa simak video berikut yaa.
