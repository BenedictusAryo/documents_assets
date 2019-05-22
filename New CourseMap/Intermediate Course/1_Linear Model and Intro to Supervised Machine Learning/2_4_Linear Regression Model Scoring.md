# 2-04 Linear Regression Model Scoring

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, ketika kita telah mendapatkan data dari aktual sama prediksi sekarang waktunya kita melakukan scoring terhadap model yang telah kita latih menggunakan syntax sebagai berikut:

```
mean_squared_error(y_test,pred)
mean_absolute_error(y_test,pred)
r2_score(y_test,pred)
```

Kemudian jika data yang dipunyai ingin dibuat grafiknya dapat menggunakan syntax sebagi berikut:

```
plt.scatter(x_test, y_test)
plt.plot(x_test,pred,color = 'r')
plt.title('Plot of Testing Data')
plt.xlabel('LSTAT')
plt.ylabel('MEDV')
plt.show()
```

Hasil syntax diatas akan mengeluarkan output sebagai berikut:

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/1_Linear%20Model%20and%20Intro%20to%20Supervised%20Machine%20Learning/assets/2019-05-17_11-28-47.png)

Nah, gimana? Makin Paham? Simak lagi yuk video selanjutnya.