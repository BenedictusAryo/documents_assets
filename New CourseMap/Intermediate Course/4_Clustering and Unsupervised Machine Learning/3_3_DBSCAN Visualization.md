# 3_3_DBSCAN Visualization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, selanjutnya pada video kali ini akan dijelaskan  bagaimana menggambarkan cluster yang didapatkan pada video sebelumnya baik tanpa scalling maupun menggunakan scalling. Berikut syntax yang digunakan.
```
model_dbs = DBSCAN(eps=0.1, min_samples=5)
X = X_sca.copy()
X
```
```
model_dbs.fit_predict(X)
labels = model_dbs.labels_
n_clusters_ = len(set(labels))-(1 if -1 in labels else 0)
n_clusters_
```
```
core_samples_mask = np.zeros_like(model_dbs.labels_, dtype=bool)
core_samples_mask[model_dbs.core_sample_indices_] = True
core_sample_mask
```
```
unique_labels = set(labels)
colors = [plt.cm.Spectral(each)
	  for each in np.linspace(0, 1, len(unique_labels))]
for k, col in zip (unique_labels, colors) :
	if k == -1
		
        # Black used for noise.
		col = [0, 0, 0, 1]

	class_member_mask = (labels == k)

	xy = X[class_member_mask & core_samples_mask]
	plt.plot(xy[:, 0], xy[:, 1], 'o',
        markerfacecolor=tuple(col), markeredgecolor='k',
        markersize=14)

	xy = X[class_member_mask & ~core_samples_mask]
	plt.plot(xy[:, 0], xy[:, 1], 'o',
        markerfacecolor=tuple(col),
        markeredgecolor='k', markersize=6)

plt.title('Estimated number of clusters: %d' % n_clusters_)
plt.show()
```
Ternyata perintah diatas menghasilkan output dibawah ini.

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/9.png)

