# Part 11

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Nah, teman-teman pada video kali ini kita akan membahas bagaimana ketika nilai *C* atau *regularization* nya berbeda. Dalam hal ini kita perlu mendefinisikan terlebih dahulu nilai parameter yang akan diisi. Pada kasus kali ini kita akan mendefinisikan parameter tersebut dengan ```param_c```. Untuk lebih jelasnya yuk simak video berikut.
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

Nah, temen-temen paham tidak sama perintah diatas? Kalau tidak, yuk lebih baik kita simak video berikut. 