# 09 Stacked Bar Chart 

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Stacked Bar Chart merupakan Barchart dari penggabungan kategori-kategori tertentu dibuat mejadi satu visualisasi. 

Pada pembelajaran kali ini akan ditampilkan visualisasi Stacked Bar Chart top 10 negara dengan mendali terbaik berdasarkan mendali Gold, Silver dan Bronze. 
```
all_go_1 = all_go.head(10)
all_go_1.loc[:, ['G','S','B']].plot.bar(stacked=True)
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_2.png" width="460" height="360" align="center"/>

Pada gambar diatas diketahui bahwa Stacked Bar Chart yang ditampilkan sumbu x masih dalam bentuk indeks. Maka diperlukan untuk mengubahnya kembali menjadi nama negara dengan perintah
```
all_go_1 = all_go_1.set_index('NOC')
all_go_1.loc[:, ['G','S','B']].plot.bar(stacked=True)
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_3.png" width="460" height="360" align="center"/>

Berdasarkan gambar diatas sumbu x telah berubah menjadi nama negara. Namun yang menjadi masalah sekarang yaitu sulitnya untuk membandingkan mendali silver dan bronze antara negara satu dengan lainnya. Nah, mari kita ganti dengan perintah
```
all_go_1.loc[:, ['G','S','B']].plot.bar()
plt.title('Total Athlete on Sport in Olympic 2016')
plt.xlabel('Total Athelete on Sport in Olympic 2016')
plt.ylabel('Sport')
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_5.png" width="460" height="360" align="center"/>

Berdasarkan gambar diatas lebih mudah untuk membandingkan semua mendali yang didapatkan oleh semua negara. Seperti USA mendapatkan gold paling banyak dan silver hapir sama dengan great britain, dst.