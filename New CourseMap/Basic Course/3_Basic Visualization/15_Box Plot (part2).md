# 16 Box Plot (part2)

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Dataset untuk Latihan pada Bab ini bisa di download di : 
[athlete_events.csv](https://drive.google.com/file/d/1M5KLfA9DpVWiKqVQ9bwjFJWcl0yl-9TX/view?usp=sharing)_

Selanjutnya dari video sebelumnya, kita akan mempelajari cara untuk membuat Box Plot. Box Plot cocok untuk data yang bertipe numerical dan categorical untuk mengatahui outlier data yang kita gunakan. 

Pada kasus ini Box Plot dibuat dari hubungan variabel Sex dan Age, hubungan variabel Sex dan Height, dan hubungan variabel Sex dan Weight. 
```
sns.boxplot(x='Sex', y='Age', data = df)
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_11.png" width="460" height="360" align="center"/>

Dari boxplot diatas didapatkan banyak data yang outlier baik dari perempuan maupun laki-laki. Persebaran umur perempuan dan laki-laki hampir sama, hanya saja perempuan terdapat beberapa atlet yang lebih tua dari pada perempuan. 
```
sns.boxplot(x='Sex', y='Height', data = df)
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_12.png" width="460" height="360" align="center"/>

Dari boxplot diatas diketahui bahwa kecendrungan data berdasarkan tinggi. Pada boxplot laki-laki persebaran tidak berbeda jauh dari pada perempuan. Tetapi, laki-laki persebaran data sedikit lebih tinggi. 
```
sns.boxplot(x='Sex', y='Weight', data = df)
plt.title('Distribution of Weight based on Sex')
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_13.png" width="460" height="360" align="center"/>

Didapatkan kecendrungan persebaran data laki-laki sedikit lebih tiggi dari pada perempuan. Outlier pada perempuan ada outlier dibawah nilai minimal sedangkan laki-laki tidak ada. 