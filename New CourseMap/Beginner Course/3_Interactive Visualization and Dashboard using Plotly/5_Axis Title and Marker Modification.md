# 05 Axis Title and Marker Modification

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini, kita akan belajar bagaimana membuat sebuah judul pada `axis`.
Untuk membuat axis kita perlu masuk terlebih dahulu ke dalam menu graph object layout baru kemudian kita menambahkan menu `xaxis` ataupun `yaxis`.

```
layout = go.layout(title='Scatterplots !',
                   xaxis={'title':'Time'},
                   yaxis={'title':'Frequency'})
```

Nah, perlu diingat bahwa ada dua cara dalam membuat sebuah judul pada bagian *axis* ketika menggunakan `dictionary`. Dalam menggunakan dictionary yang pertama yaitu pada bagian **title** digunakan tanda petik. Namun, dapat juga menggunakan `dictionary` dengan "tanda kurung kurawal" seperti dibawah ini:

```
layout = go.layout(title='Scatterplots !',
                   xaxis=dict(title='Time'),
                   yaxis=dict(title='Frequency'))
```
Perlu diketahui bahwa tidak masalah ingin menggunakan metode yang mana karena akan menghasilkan output yang sama. Namun, perlu diingat bahwa `dictionary` menggunakan kurung kurawal perlu di set dengan tipe string, lalu menggunakan tanda petik, dan titik dua. 

Selain itu, kita dapat memodifikasi pada bagian **marker**. Seperti memodifikasi pada bagian warna, size, simbol, dan sebagainya.

Untuk list marker symbol dapat dilihat pada referensi berikut: <br>
[https://plot.ly/python/reference/#scatter](https://plot.ly/python/reference/#scatter)