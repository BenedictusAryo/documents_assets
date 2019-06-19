# 2_2_Data Plotting

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**


Video kali ini merupakan lanjutan dari video sebelumnya. Sebelum kita melakukan pemodelan pada **clustering** yang perlu dlakukan ialah kita harus tau bentuk plot dari data yang dimiliki. 
```
data_clu.info()
plt.scatter(data_clue['Distance_Feature'], data_clu['Sp e  eading_Feature'])
plt.xlabel('Distance Feature')
plt.ylabel ('Speeding Feature')
plt.show()
```
Hasil diatas akan menghasilkan output sebagai berikut.

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/7.png)

Dari sebaran data tersebut, kita akan menguji apakah model `clustering` yang kita buat mampu mempelajari pola-pola yang terlihat pada data tersebut.
