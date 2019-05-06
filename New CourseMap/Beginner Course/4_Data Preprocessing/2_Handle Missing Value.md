# 01 Handle Missing Value

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada pembelajaran kali ini kita akan mempelajari untuk meng-handle missing value atau adanya data-data yang kosong. 

Pada pembahasan kali ini menggunakan data ```train.csv```. Sebelumnya, mari kita input data tersebut dengan perintah
```
df = pd.read_csv('data/train.csv')
df.head()
```
*Output :*

| PassengerId | Survived | Pclass | Name                                                | Sex    | Age  | SibSp | Parch | Ticket           | Fare    | Cabin | Embarked |
|-------------|----------|--------|-----------------------------------------------------|--------|------|-------|-------|------------------|---------|-------|----------|
| 1           | 0        | 3      | Braund, Mr. Owen Harris                             | male   | 22.0 | 1     | 0     | A/5 21171        | 7.25    |       | S        |
| 2           | 1        | 1      | Cumings, Mrs. John Bradley (Florence Briggs Thayer) | female | 38.0 | 1     | 0     | PC 17599         | 71.2833 | C85   | C        |
| 3           | 1        | 3      | Heikkinen, Miss. Laina                              | female | 26.0 | 0     | 0     | STON/O2. 3101282 | 7.925   |       | S        |
| 4           | 1        | 1      | Futrelle, Mrs. Jacques Heath (Lily May Peel)        | female | 35.0 | 1     | 0     | 113803           | 53.1    | C123  | S        |
| 5           | 0        | 3      | Allen, Mr. William Henry                            | male   | 35.0 | 0     | 0     | 373450           | 8.05    |       | S        |

Pada output data diatas terdapat beberapa nilai kosong. Untuk melihat nilai kosong dengan mudah dengan perintah
```
pd.isnull(df).sum()
```
*Output :*
```
PassengerId      0
Survived         0
Pclass           0
Name             0
Sex              0
Age            177
SibSp            0
Parch            0
Ticket           0
Fare             0
Cabin          687
Embarked         2
dtype: int64
```

Dari output diatas didapatkan nilai yang kosong yaitu variabel Age dengan 177 data yang kosng, Cabin dengan 687 data yang kosong dan Embarked dengan 2 data yang kosong. 