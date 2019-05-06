# 14 Training and Testing Data

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Sebelum kita masuk ke Mechine Learning, sebelumnya kita butuh untuk membagi data training dan data testing. Baik, sebelumnya kita perlu import pacakge berikut

```
from sklearn.model_selection import train_test_split
```

Selanjutnya, kita bagikan data X (feature) dan data y (target)

```
X = data_fix.drop(columns='Survived')
y = data_fix['Survived']
```

Data y (target) yaitu kolom ```Survived``` dan data X (feature) yaitu kolom selain ```Survived```. Oleh karena itu pada data X kolom ```Survived``` dihapus. Mari kita bagi data testing dan training dengan perintah

```
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=45)
```

Pada syntax diatas dibagilah data X dan y untuk training dan testing dengan data testing yang dipilih hanya 20%, jadi data trainingnya 80%. Kita dapat melihat jumlah data training dan data testing dengan perintah berikut

```
X_train.shape
```

*Output :* 

(712, 12)

```
X_test.shape
```

*Output :* 

(179,12)

Dari ouput diatas jadi data training yang digunakan yaitu 712 baris sedangkan testing 179 baris.