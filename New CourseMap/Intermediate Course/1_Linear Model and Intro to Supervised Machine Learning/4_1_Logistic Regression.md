# 4-01 Logistic Regression

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas terkait `Logistic Regression` . Untuk dataset logistik regression dapat di download pada link berikut.

[Default.csv](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/1_Linear%20Model%20and%20Intro%20to%20Supervised%20Machine%20Learning/assets/Default.zip)

```
data_log = pd.read_csv('data/Default.csv')
data_log.head()
```
Nah, ketika data telah di-load, ada beberapa hal yang harus di pre-processing, diantaranya yaitu yang pertama adalah mengubah variabel `default` dan `student` kedalam bentuk angka menggunakan syntax berikut:
```
data_log = data_log.drop('Unnamed: 0', axis = 1)
data_log.head()
```

```
data_log.loc[data_log['default']=='No';'default'] = 0
data_log.loc[data_log['default']=='Yes';'default'] = 1
```
```
data_log.loc[data_log['student']=='No','student'] = 0
data_log.loc[data_log['student']=='Yes','student'] = 1
```
Nah, untuk penjelasannya bisa simak video berikut yuk.
