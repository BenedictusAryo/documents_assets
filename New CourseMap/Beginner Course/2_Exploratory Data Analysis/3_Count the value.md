# 03 Count the value

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Seperti yang telah dijelaskan sebelumnya, bahwa salah satu fungsi Exploration Data Analysis adalah untuk menjawab pertanyaan dengan data. Jadi, pada video ini kita akan lebih mendalami tentang bagaimana kita menjawab berbagai pertanyaan dengan data yang kita miliki.

*Contoh Pertanyaan :*
>**How many total country in each continents from the datasets ?**

Nah, pada function describe seperti yang dijelaskan pada video sebelumnya, kita dapat mengetahui jumlah baris yang terdapat pada kolom *country*, yakni ada **193**, namun pertanyaan nya adalah berapa jumlah negara pada tiap benua yang terdapat pada dataset kita ? <br>
Untuk menjawab pertanyaan tersebut, kita dapat menggunakan perintah *value_counts*.
```
df["continent"].value_counts()
```
*Output :*
```
Africa           53
Europe           45
Asia             44
North America    23
Oceania          16
South America    12
Name: continent, dtype: int64
```

Command ```df["continent]``` kita gunakan, karena kita hendak mengambil kolom *continent*-nya saja untuk kita kelompokkan, kemudian kita menambahkan perintah ```value_counts()``` untuk menghitung berapa jumlah data pada tiap-tiap benuanya.<br>
Maka kita akan mendapatkan informasi jumlah negara yang terdapat pada tiap-tiap benua pada dataset kita.