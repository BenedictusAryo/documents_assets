# 2_5_Result Visualization Part-2
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

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/3_Decision%20Tree%2C%20Random%20Forest%20and%20Gradient%20Boosting/assets/2.png)

Teman-teman kin telah mengetahui bagaimana model yang telah teman-teman buat serta bagaimana kompleksitasnya menyelesaikan masalah klasifikasi data tersebut.