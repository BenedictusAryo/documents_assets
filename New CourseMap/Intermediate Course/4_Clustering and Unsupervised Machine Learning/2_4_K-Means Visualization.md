# 2_4_K-Means Visualization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mendapatkan hasil prediksi dari data yang dimiliki namun hasil tersebut tidak dapat kita baca karena berbentuk angka 0 dan 1. Pada video kali ini kita akan mengubah hasil prediksi tersebut ke dalam bentuk visualisasi yang mudah untuk dipahami menggunakan syntax sebagai berikut.

```
plt.tigh_layout()
plt.subplot(121)
plt.scatter(data_clu['Distance_Feature'], data_clu['Speeding_Feature'], c = pred_kme)
plt.xlabel('Distance Features')
plt.ylabel('Speeding Feature')
plt.title('2 Cluster')

plt.subplot(122)
plt.scatter(data_clu['Distance_Feature'], data_clu['Speeding_Feature'], c = pred_kme_2)
plt.xlabel('Distance Features')
plt.ylabel('Speeding Feature')
plt.title('4 Cluster')

plt.show()
```

Untuk perintah diatas akan menghasilkan output dibawah ini.

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/8.png)

Output diatas menunjukkan 2 hasil yaitu hasil pertama untuk visualisasi 2 cluster dan hasil kedua menunjukkan hasil untuk visualisasi 4 cluster. Lalu, manakah yang lebih baik? Untuk lebih jelasnya yuk simak video setelah ini. 