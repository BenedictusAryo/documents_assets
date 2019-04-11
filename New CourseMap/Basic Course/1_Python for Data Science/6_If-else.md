# 06 If - else

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pernyataan if - else merupakan pernyataan pada python yang menyatakan decision making.
pernyataan ini berfungsi ketika kita membutuhkan suatu pemilihan keputusan pada script kita.

```
a = 3
b = 5

if a > b :
    print ("a Lebih dari b")
else :
    print("a Kurang dari b")
```
*Output:*

```
a Kurang dari b
```

Pada contoh diatas, kita menggunakan *if* untuk menentukan apakah a lebih besar dari b. 

Perlu dicatat, ketika kita menggunakan **else**, maka **kita tidak perlu menambahkan pernyataan kondisi setelah else**, karena python akan otomatis mengelompokkan, kondisi **selain a > b menjadi "a Kurang dari b"**.

Namun apabila kondisinya adalah *a = b*, maka python akan tetap menganggap **"a Kurang dari b"**
```
a = 3
b = 3

if a > b :
    print ("a Lebih dari b")
else :
    print("a Kurang dari b")
```
*Output:*

```
a Kurang dari b
```
Nah, bagaimana mengatasi kondisi seperti ini, simak video selanjutnya.


