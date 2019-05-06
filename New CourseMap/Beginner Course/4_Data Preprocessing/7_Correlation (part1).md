# 06 Correlation 1

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pembahasan kali ini yaitu membahas tentang korelasi. Telah dibahas pada pertemuan sebelumnya nilai korelasi mempunyai nilai -1 sampai 1. 

Kita akan kembali menggunakan data titanic pada video awal bab ini.

Untuk memudahkan membaca korelasi lebih baik dengan menggunakan visualisasi dengan perintah

```
import seaborn as sns
y_feat = df.corr()
sns.heatmap(y_feat, vmax = 1, vmin = -1, xticklabels= y_feat.columns, yticklabels = y_feat.columns, annot=True);
```

*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/4_Data%20Preprocessing/Assets/Figure_3.png" width="360" height="290" align="center"/>

Pada hasil diatas didapatkan lebh menarik dengan tampilan warna, maka kuatnya korelasi selain dapat dilihat dari angka juga bisa dilihat dari warna. 