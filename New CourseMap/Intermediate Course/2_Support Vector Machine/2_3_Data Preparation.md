# 2_3_Data Preparation

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah sampai pada loading data dimana kita menggunakan **data iris** untuk melakukan klasifikasi dengan metode **SVM**. Pada video kali ini kita akan membahas mengenai tahapan selajutnya yaitu melakukan preprocessing sederhana pada data kita tersebut.

Dimana, yang pertama dilakukan yaitu membuat label nama pada data yang dipunyai sebagai berikut.

```
label_enc = LabelEncoder()
```

Kemudian, dilakukan fitting data, sebagai berikut:

```
label_enc.fit(data['species'])
label_enc.classes_
enc = label_enc.transform(data['species'])
```

```
enc_fix = pf.DataFrame(enc)
enc_fix.columns = ['new_species']
enc_fix.head()
```

Langkah terakhir pada light processing ini yaitu menggabungkan data yang sudah diolah sebelumnya, sebagai berikut.
```
data = data.join(enc_fix)
data.head()
```