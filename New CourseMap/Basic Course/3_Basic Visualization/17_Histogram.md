# 17 Histogram

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Histogram visualisasinya hampir sama dengan Bar Chart dari pembahasan sebelumnya. Tetapi, Bar Chart digunakan untuk data yang bertipe categorical sedangkan Histogram untuk data yang bertipe Numerical. 

Perbedaan yang lain yaitu pada Bar Chart visualisasi antar batang akan ada spasinya atau jaraknya. Sedangkan,  pda Histogram visualisasi antar batang akan berdempetan. 

Pada oembelajarn kali ini kita akan mencoba membuat histogram dari variabel ```Sex```.
```
sns.distplot(df['Age'], kde=False)
plt.ylabel('Count')
plt.title('Distribution of Age in Olympics')
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_14.png" width="460" height="360" align="center"/>

Dari histogram diatas dapat didapatkan informasi atlet yang paling banyak mengikuti olympiade yaitu dengan umur 20-30 tahun. 
