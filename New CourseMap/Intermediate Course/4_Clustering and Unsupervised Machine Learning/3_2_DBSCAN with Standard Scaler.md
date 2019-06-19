# 3_2_DBSCAN with Standard Scaler

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, sekarang bagaimana jika menggunakan *Scalling*. Apakah akan menghasilkan jumlah cluster yang berbeda atau justru sama? Untuk melakukan **clustering DBSCAN** menggunakan *Scalling* kita perlu mengimport ```StandardScaler```.
```
from sklearn.preprocessing import StandardScaler
X_sca = StandardScaler().fit_transform(X)
X_sca
```
```
model_dbs.fit_predict(X_sca)
labels = model_dbs.labels_
n_clusters_ = len(set(labels)) - (1 if -1 in labels else 0)
n_clusters_
```
Hasi output diatas menunjukkan ternyata didapatkan kesimpulan cluster menjadi tidak terbaca sama sekali dan hanya terbaca satu cluster saja ketika kita menggunakan *Scalling*. Kok bisa gitu ya? Lebih baik simak penjelasan video berikut yuk.