# 08 Barplot Grouped and Stackmode

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya membuat sebuah **bar plot**. <br>
**Bar plot** adalah sebuah grafik yang berbentuk batang dengan nilai x-axis berbentuk kategorik dan nilai y-axis berbentuk numerik.

Langkah awal yaitu mengimport data frame dengan memanggil beberapa packages diantaranya **pandas** , **plotly.offine** , dan **plotly.graph_objs** pada library.

Kemudian, untuk membuat barplot dapat digunakan perintah sebagai berikut:

```
data=[go.Bar(
    x=df['NOC'],
    y=df['Total'])]
```
```
layout = go.Layout(title='2018 Olympics Medal by 
Country',xaxis=dict(title='Country'),yaxis={'title':'Total Medals'})
```
```
fig = go.Figure(data=data, layout=layout)
```
```
pyo.plot(fig,filename='barplot.html')
```
Perintah diatas kemudian dijalankan dan akan menghasilkan bar plot sebagai berikut:

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/3_Interactive%20Visualization%20and%20Dashboard%20using%20Plotly/assets/8_Barplot_total.png)

Grafik bar plot diatas merupakan bar plot yang menunjukkan total medali yang ingin diketahui. Lalu, bagaimana jika ingin mengetahui perolehan tiap jenis medalinya? <br>
Untuk mengetahui perolehan dari tiap jenis medalinya dapat menggunakan **Grouped Bar Plot**. Contohnya, sebagai berikut: 

```
gold = go.Bar(x=df['NOC'],
              y=df['Gold'],
              name='Gold',
              marker=dict(color='gold'))
```
```
silver = go.Bar(x=df['NOC'],
                y=df['Silver'],
                name='Silver',
                marker=dict(color='silver'))
```
```
bronze = go.Bar(x=df['NOC'],
                y=df['Bronze'],
                name='Bronze',
                marker=dict(color='brown'))
```
```
data = [gold, silver, bronze]
```
Kemudian dijalankan dan akan menghasilkan output sebagai berikut:

![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/3_Interactive%20Visualization%20and%20Dashboard%20using%20Plotly/assets/9_Barplot_groped.gif)

Lalu, gimana caranya jka kita tetap ingin mendapatkan informasi total perolehan medalinya dari hasil sebelumnya?<br>
Dalam hal ini mudah sekali dilakukan hanya dengan mengganti **barmode = 'stack'** pada bagian layout seperti berikut:<br>
```
layout = go.Layout(title = '2018 Olympics Medal by Country',                      
                   xaxis=dict(title='Country'),
                   yaxis={'title':'Total Medals'},
                   barmode='stack')
```
![assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/3_Interactive%20Visualization%20and%20Dashboard%20using%20Plotly/assets/10_Barplot_stacked.gif)

Nah, perlu diperhatikan juga ya bahwa di `plotly` ini framework nya banyak menggunakan `dictionary` maupun `tuple` maka diharapkan berhati-hati dikarenakan rawan sekali terjadi kesalahan. <br>



