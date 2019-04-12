# 18 Heatmap

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Heatmap digunakan untuk mengatahui korelasi antar data dengan warna yang menarik. Nah, pada Heatmap ini selain kita bisa melihat besar korelasi dengan menggunakan angka, kita bisa juga  melihat korelasi melalui warna. Korelasi nilanya yaitu -1 sampai 1. Ketika nilai  mendekati 1 (korelasi positif) dan -1 (korelasi negatif) maka nilai tersebut berkorelasi kuat. 

Pada kasus ini kita ingin mencari korelasi dari tabel ```all_go```. Perlu diketahui korelasi digunakan untuk data yang numerik. 
```
sns.heatmap(all_go.corr(), annot=True, cmap='RdBu')
plt.plot()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_15.png" width="460" height="360" align="center"/>

Didapatkan nilai korelasi dengan angka dan warna. 
