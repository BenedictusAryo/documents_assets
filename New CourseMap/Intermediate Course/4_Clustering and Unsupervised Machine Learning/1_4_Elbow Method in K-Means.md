# 1_4_Elbow Method in K-Means 

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Berdasarkan video sebelumnya kita telah mengetahui tentang **k** dan **centroid**. Nah, pada video kali ini kita akan mempelajari bagaimana caranya menentukan **k** terbaik yang merupakan jumlah cluster. 

Dalam penentuan **k** terbaik kita dapat menggunakan *Elbow Method*

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/2.png)

Pada *Elbow Method* nilai Axis Title merupakan *error rate* dimana pengaruh dari *error rate* ini ialah seberapa bagus cluster tersebut tidak memiliki error. Lalu cara membaca *Elbow Method* yaitu berdasarkan nilai yang paling ekstrim turunnya.

Sehingga pada grafik diatas, kasus tersebut akan sangat optimum apabila K-Means yang kita buat adalah dengan `k=3`.