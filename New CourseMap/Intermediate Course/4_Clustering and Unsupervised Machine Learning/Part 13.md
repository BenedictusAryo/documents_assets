# Part 13

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas mengenai penggunaan clustering dengan **DBSCAN Without Scalling**. <br>
Langkah pertama yaitu kita memanggil model DBSCAN terlebih dahulu.
```
model_dbs = DBSCAN(eps=1 , min_samples=5)
model_dbs.fit_predict (X)
labels = model_dbs.labels_
n_clusters_ = len(set(labels))-(1 if -1 in labels else 0)
n_clusters_
```
Didapatkan kesimpulan ketika menggunakan **DBSCAN Without Scalling** cluster yang dihasilkan berjumlah 26. Lalu, bagaimana jika kita menggunakan **DBSCAN With Scalling** apakah ada perbedaan ? Yuk, simak video selanjutnya. 