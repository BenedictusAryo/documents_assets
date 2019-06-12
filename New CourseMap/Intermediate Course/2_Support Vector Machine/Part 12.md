# Part 12

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan membahas mengenai bagaimana caranya mengganti nilai *Gamma* dan *Kernel* pada data. Pada dasarnya syntax untuk mengganti nilai tersebut hampir sama seperti syntax pada video sebelumnya. Lalu, yang membedakan itu apa sih? Perhatikan syntax berikut ya...
```
param_gamma = [0.001, 0.01, 0.1, 1, 10, 100]
plt.figure(figsize=(12,7))
plt.suptitle('Different Type of Gamma)
for i in range(6):
    plt.subplot(2,3,i+1)
    model = SVC(gamma = param_gamma[i])
    model.fit(X_train, y_train)
    plot_decision_regions(X = X_test.values, y = y_test.values, clf = model, legend = 2)
    plt.title(param_gamma[i])
```
Kemudia, untuk kernel nya sebagai berikut ya.
```
param_kernel = ['rbf','linear','sigmoid','poly']
plt.figure(figsize = (10,10))
plt.suptitle('Different Type of C')
for i in range (4):
    plt.subplot(2,2,i+1)
    model = SVC(C = param_kernel[i])
    model.fit(X_train, y_train)
    plot_decision_regions(X = X_test.values, y = y_test.values, clf = model, legend = 2)
    plt.title('%s \n Score:%1.2f' %(param_kernel[i], model.score(X_test, y_test)))
```
Nah, ternyata syntax diatas menghasilkan output berikut lho...

![Assets](https://www.dropbox.com/sh/3escqhuxix16hj2/AADqs3tUYYtxlUvXQci-HUUPa/6.png?dl=1)

Bagaimana? Apakah paham sama hasil output diatas? Kalau belum paham, yuk simak video berikut.