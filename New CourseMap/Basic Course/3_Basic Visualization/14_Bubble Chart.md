# 14 Bubble Chart

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Bubble Chart visualisasi yang mirip dengan Scatter Plot hanya saja bisa menampilkan data tambahan dengan menampilkan ukuran-ukuran tertentu. 

Pada kasus ini menggunakan ```all_go``` (data perolehan mendali setiap negara) dari video sebelumnya dengan sumbu x yaitu Total atlet dan sumbu y yaitu Total Mendali dengan ukuran bersadasarkan Gold. 
```
sns.scatterplot(x='Total', y='Total_Medals', size='G',hue='G', data=all_go)
plt.show()
```
*Output :*

<img src ="https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Basic%20Course/3_Basic%20Visualization/Assets/Figure_10.png" width="460" height="360" align="center"/>

Dari output diatas terlihat besar dan warna setiap titik berbeda-beda sesuai dengan banyaknya Gold yang didapatkan setiap negara. Jadi selain hubungan total atlet dan total mendali, ada informasi tambahan yaitu banyaknya Gold yang kita dapatkan dari bubble chart diatas. 