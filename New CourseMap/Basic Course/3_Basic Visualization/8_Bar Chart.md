# 08 Bar Chart

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Visualisasi data yang pertama yang kita pelajari yaitu Bar Chart. Bar Chart yaitu visualisasi dengan menggunakan batang bisa dalam bentuk vertikal maupun horizontal. 


Pada pembelajaran kali ini, kita akan coba frekuensi olahraga (variabel Sport) dengan menggunakan Bar Chart dengan perintah berikut 
```
plt.figure(figsize=(12,12))
df['Sport'].value_counts().plot(kind='barh')
plt.title('Total Athlete on Sport in Olympic 2016')
plt.xlabel('Total Athelete on Sport in Olympic 2016')
plt.ylabel('Sport')
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_1.png" width="560" height="460" align="center"/>

Dari gambar diatas didapatkan olahraga terbanyak yaitu atletik, terbanyak kedua yaitu renang, dan seterusnya dapat dilihat pada gambar diatas. 
