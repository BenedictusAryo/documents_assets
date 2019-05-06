# 03 fillna Function

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan membahas tentang fillna function. Pada video sebelumnya kita menggunakan dropna function untuk menghapus data kosong, sedangkan fillna kali ini digunakan untuk mengisi data yang kosong dengan suatu nilai. 

Pada kasus ini mengisi data-data kosong pada kolom ```Age``` dengan median data tersebut

```
df1 = df1.fillna({'Age':df1['Age'].median()})
```

Mari kita kita lihat info dari data df1 dengan perintah

```
df1.info()
```

*Output :*

```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 891 entries, 0 to 890
Data columns (total 12 columns):
PassengerId    891 non-null int64
Survived       891 non-null int64
Pclass         891 non-null int64
Name           891 non-null object
Sex            891 non-null object
Age            891 non-null float64
SibSp          891 non-null int64
Parch          891 non-null int64
Ticket         891 non-null object
Fare           891 non-null float64
Cabin          204 non-null object
Embarked       889 non-null object
dtypes: float64(2), int64(5), object(5)
memory usage: 83.6+ KB
```

Dapat dilihat bahwa nilai dari kolom ```Age``` telah terisi semua dengan data 891 data. 

Selanjutnya dari kolom data ```Embarked``` . Dikarenakan data yang terdapat pada kolom ```Embarked``` bertipe kategorical maka digunakan penambahan data kosong dengan nilai modus. Sebelumnya mari kita lihat terlebih dahulu modus dari kolom tersebut

```
df1['Embarked'].value_counts()
```

*Output :*

```
S   644
C   168
Q    77
Name: Embarked, dtype: int64
```

Dari data diatas ternyata yang paling banyak datanya yaitu ```S```. Kemudian, kita akan masukkan data S tersebut kedalam data yang kosong pada kolom ```Embarked```

```
df1 = df1.fillna({'Embarked':'S'})
```

Mari kita lihat info data tersebut

```
df.info()
```

*Output :*

```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 891 entries, 0 to 890
Data columns (total 12 columns):
PassengerId    891 non-null int64
Survived       891 non-null int64
Pclass         891 non-null int64
Name           891 non-null object
Sex            891 non-null object
Age            891 non-null float64
SibSp          891 non-null int64
Parch          891 non-null int64
Ticket         891 non-null object
Fare           891 non-null float64
Cabin          204 non-null object
Embarked       891 non-null object
dtypes: float64(2), int64(5), object(5)
memory usage: 83.6+ KB
``` 

Dari info tersebut kolom ```Embarked``` telah terisi semua. 