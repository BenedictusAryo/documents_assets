# Part 8

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Nah, pada video kali ini kita akan membahas terkait bagiamana caranya memilih fitur yang baik. Perlu diketahui bahwa dalam melakukan penentuan fitur, salah satu hal yang dapat dilakukan ialah dengan melihat pada korelasi.

Setelah mendapatkan 2 fitur yang mempunyai korelasi yang cukup tinggi pada target, selanjutnya kita dapat melakukan train test split. Untuk syntax yang digunakan yaitu sebagai berikut. 
```
X = data[['Glucose','BMI']]
y = data['Outcome']
X_train, X_test, y_train, y_test = train_test_split(X,y, test_size=0.2,random state=45)
y_train.value_counts()
y_test.value_counts()
```