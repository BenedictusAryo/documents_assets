# 06 Filter Sort Values 

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video sebelumnya, kita telah mempelajari tentang dataframe filtering untuk menjawab pertanyaan dengan data. Nah, pada video kali ini kita akan membahas tentang value sorting lewat pertanyaan berikut : 

>**What is the country that consumes the most spirit in Africa?**

Nah, untuk menjawab pertanyaan ini, kita dapat menjawabnya dengan 2 langkah, yakni **pertama** filter country Africa terlebih dahulu, **kedua** kita melakukan sorting value dengan jenis **descending** atau menurun pada kolom **spirit_servings**. dengan langkah tersebut, kita akan mendapatkan informasi negara Africa dengan konsumsi spirit paling banyak pada data kita.

```
# membuat variable africa yang berisi hanya negara di kolom 'continent' Africa
africa = df[df['continent] == 'Africa]

# kemudian membuat variable africa_spirit 
# untuk melakukan sorting descending pada kolom 'spirit_servings'
africa_spirit = africa.sort_values(by=['spirit_servings'], ascending=False)

# kemudian kita hendak menampilkan tabel africa_spirit 
# pada baris pertama saja, yakni yang memiliki konsumsi spirit paling tinggi
africa_spirit[:1]

```
*Output :*
| country | beer_servings | spirit_servings | wine_servings | total_litres_of_pure_alcohol | continent |
|---------|--------------:|----------------:|--------------:|-----------------------------:|-----------|
| Liberia | 19            | 152             | 2             | 3.1                          | Africa    |
|         |               |                 |               |                              |           |

Nah, sekarang kita tahu bahwa negara di Africa yang memiliki konsumsi spirit tertinggi adalah **Liberia**.

Script di atas juga bisa disingkat menjadi 1 baris saja karena python merupakan bahasa pemrograman OOP atau Object Oriented programming. Berikut adalah perintah yang sama dalam bentuk 1 baris.

```
df[df['continent] == 'Africa].sort_values(by=['spirit_servings'], ascending=False).head(1) 
#head(1) digunakan untuk menampilkan 1 baris paling awal saja
```
*Output :*
| country | beer_servings | spirit_servings | wine_servings | total_litres_of_pure_alcohol | continent |
|---------|--------------:|----------------:|--------------:|-----------------------------:|-----------|
| Liberia | 19            | 152             | 2             | 3.1                          | Africa    |
|         |               |                 |               |                              |           |