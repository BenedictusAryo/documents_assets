# Part 12

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Berdasarkan hasil yang didapatkan pada video sebelumnya, kita perlu menentukan cluster manakah yang terbaik. Dalam penentuan cluster dapat menggunakan *Elbow Method*. Namun, sebelum mendapatkan nilai *Elbow Method* kita perlu menggunakan data yang baik terlebih dahulu.
```
distortions = []
K = range (1, 10)
for k in K:
    kmeanModel = KMeans(n_clusters=k).fit(X)
    distortions.append(sum(np.min(cdist(X, kmeanModel.cluster_centers_,'euclidean'),axis=1))/ X.shape[0])

# plot the elbow
plt.plot(K, distortions, 'bx-')
plt.xlabel('k')
plt.ylabel('Distortion')
plt.title('The Elbow Method showing the optimal k')
plt.show()
```
Maka akan menghasilkan grafik elbow seperti dibawah ini :

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/12.png)
