# Part 7

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mengimport packages serta data yang akan digunakan Perlu diketahui bahwa target untuk case study kali ini yaitu kita ingin memprediksi mana yang terkena penyakit diabetes dan yang tidak terkena penyakit diabetes. Nah, pada video kali ini kita akan melakukan analisa singkat terkait data. Syntax yang dibutuhkan untuk analisa yaitu sebagai berikut.
```
data['Outcome'].value_counts()
data.info()
data.describe()
```
```
X = data ['Pregnancies','Glucose']
y = data ['Outcomes']
```