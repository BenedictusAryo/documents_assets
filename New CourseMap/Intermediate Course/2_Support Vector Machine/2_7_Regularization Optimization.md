# 2_7_Regularization Optimization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Nah, teman-teman pada video kali ini kita akan membahas bagaimana ketika nilai *C* atau *regularization* nya berbeda ?

Kita akan melakukan `hyperparameter tuning` yakni dengan mengubah nilai dari parameter **C** sehingga diharapkan akan menghasilkan akurasi yang lebih baik.

Dalam hal ini kita perlu mendefinisikan terlebih dahulu nilai parameter yang akan diisi. Pada kasus kali ini kita akan mendefinisikan parameter tersebut dengan ```param_c```. Untuk lebih jelasnya yuk simak video berikut.

```
param_c = [0.001, 0.01, 0.1, 1, 10, 100]
plt.figure(figsize=(12,7))
plt.suptitle('Different Type of C')
for i in range (6):
    plt.subplot(2,3,i+1)
    model = SVC(C = param_c[i])
    model.fit(X_train, y_train)
    plot_decision_regions(X = X_test.values, y = y_test.values, clf = model, legend = 2)
    plt.title(param_c[i])
    plt.show()
```

