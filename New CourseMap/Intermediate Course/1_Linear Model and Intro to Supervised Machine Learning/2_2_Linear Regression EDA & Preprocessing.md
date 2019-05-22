# 2-02 Linear Regression EDA & Preprocessing

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan mengenai bagaimana cara transformasi data untuk `linear regression`. Nah, pada video kali ini akan dijelaskan bagaimana cara kita menggunakan `linear regression` dalam kasus ini.

Pada video sebelumnya kita telah melakukan transformasi pada target variabel data yang kita punya. Dimana dalam hal ini targetnya ialah **MEDV**. 

Sebelum melakukan `linear regression` yang pertama dilakukan ialah kita harus memilih fitur atau variabelnya terlebih dahulu untuk dipasangkan dengan target. Dalam pemilihan variabel/fitur kita dapat mencari korelasiya terlebih dahulu menggunakan syntax berikut:
```
data_lin.cor()['MEDV'][:]
```
Jika sudah mendapatkan variabel/fitur nya maka kita dapat mendefinisikan target dan fitur kedalam nilai x dan y sebagai berikut:
```
x = data_lin[['LSTAT]]
y = data_lin['MEDV']
```
Kemudian, jika nilai dari x dan y telah di definisikan maka selanjutnya kita dapat me-load fungsi regression pada python dengan syntax sebagai berikut:
```
clf = LinearRegression()
clf
```
Setelah itu kita dapat membagi data ke dalam data train dan test menggunakan syntax berikut:

```
x_train, x_test, y_train, y_test = train_test_split(x,y,test_size = 0.2, random_state = 45)
```

Nah, untuk penjelasan lebih lengkapnya, yuk kita simak pada video berikut ini.