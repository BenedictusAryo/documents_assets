# Part 16

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**


Kalau pada video sebelumnya telah membahas mengenai K-Means serta DBSCAN. Maka, pada video kali ini kita akan membahas mengenai **Hierarcical Clustering**.<br>
Untuk data yang digunakan kita menggunakan data baru yang berbeda dari data sebelumnya. 
```
data = np.array([[5,3],[10,15],[15,12],[24,10],[30,30],[85,70],[71,80],[60,78],[70,55],[80,91],])
data
```
Setelah mengimport data yang digunakan maka selanjutnya membuat scatter untuk melihat visualisasi dari data yang dimiliki. 
```
labels = range(1, 11)
plt.figure(figsize=(10, 7))
plt.subplots_adjust(bottom=0.1)
plt.scatter(data[:,0], data[:, 1], label= 'True Position')

for label, x, y in zip(labels, data [:, 0], data[:, 1]):
    plt.anotate(label, xy = (x,y), xytext = 
    (-3,3),textcoords='offset points', ha='right',
    va='bottom')
    
plt.show()
```
Sehingga data yang telah kita buat tadi akan menghasilkan output dibawah ini  

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/4_Clustering%20and%20Unsupervised%20Machine%20Learning/assets/10.png)

