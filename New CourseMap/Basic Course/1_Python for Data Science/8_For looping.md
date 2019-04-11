# 08 For loop

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
For - loop digunakan ketika kita membutuhkan script untuk menjalankan perintah yang berulang.

seperti pada contoh di video,
```
print(1)
print(2)
print(3)
print(4)
```
dapat disingkat menjadi :
```
for i in range(1,5):
    print(i)
```
*Output :*
```
1
2
3
4
```
*range* pada script di atas menggenerate nilai dari 1, sampai sebelum 5, yakni dalam kasus ini adalah 4.

for loop juga dapat digunakan untuk operasi matematika pada list.

contoh, kita memiliki list1 berisi sekumpulan angka, kita hendak menambah setiap elemenya dengan 2.
```
list1 = [1,2,3,4]
list2 = []

for i in list1:
    list2.append(i + 2)

print(list2)
```
*Output :*
```
[3, 4, 5, 6]
```