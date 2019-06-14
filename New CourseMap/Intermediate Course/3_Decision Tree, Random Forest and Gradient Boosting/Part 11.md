# Part 11

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya, kita telah menuliskan perintah untuk mem-visualisasikan data yang dipunyai. Lalu, bagaimana caranya kita membuat sebuah perintah perulangan agar hasil pada syntax di video sebelumnya dapat keluar? Perhatikan syntax berikut.
```
for i in range(3):
    plt.subplot(1,3,i+1)
    plot_decision_regions(X = X_test.values, y=y_test.values, clf = model[i],
    legend = 2)

    plt.title("Model:%s \n Score:%1.2f" % (model_name[i], model[i].score(X_test,y_test)))
```
Syntax diatas akan menghasilkan output sebagai berikut.

![Assets](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AACO4MRH-wWVkGYCM0i8JM_ta/2.png?dl=1)

Gimana? Sudah paham sama hasil output diatas? Kalau belum, yuk simak video berikut.