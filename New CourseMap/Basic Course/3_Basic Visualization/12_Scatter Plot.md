# 13 Scatter Plot

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Dataset untuk Latihan pada Bab ini bisa di download di : 
[athlete_events.csv](https://drive.google.com/file/d/1M5KLfA9DpVWiKqVQ9bwjFJWcl0yl-9TX/view?usp=sharing)_

Scatter Plot merupakan titik data dari hubungan antara variabel pada sumbu x dan sumbu y. Pada kasus ini kita akan mengetahui persebaran data dari hubungan antara nilai sumbu x (```Height```) dan sumbu y (```Weight```). 
```
sns.scatterplot(x='Height', y='Weight', data=df)
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_8.png" width="460" height="360" align="center"/>

Didapatkan scatter plot dari gambar diatas mempunyai pengaruh positif karena scatter plot yang didapatkan semakin besar ```Height``` semakin besar ```Weight``` pada banyak hubungan data. Mari kita mencoba untuk melihat dari rata-rata setiap negara
```
average = df.groupby('NOC')['Height','Weight'].mean()
sns.scatterplot(x='Height', y='Weight', data=average)
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_9.png" width="460" height="360" align="center"/>

Pada output diatas didapatkan nilai rata-rata ```Height``` dan ```weihght``` dari masing-masing negara. Didapatkan ketika ```Height``` semakin besar maka ```Weight``` semakin besar pula. 