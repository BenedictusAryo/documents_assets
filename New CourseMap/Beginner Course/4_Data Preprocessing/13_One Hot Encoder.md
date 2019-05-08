# 12 One Hot Encoder

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
One Hot Encoder merupakan metode normalisasi data kategorik dengan nilai 0 dan 1. Berbeda dengan Label Encoder, One Hot Encoder mengubah data dengan banyak kolom.
Contoh : 

       data_raw  = [France, Belgium, Germany, France, Germany]
       data_norm = [[1,0,0],[0,1,0],[0,0,1],[1,0,0],[0,0,1]]

```
from sklearn.preprocessing import OneHotEncoder

encoder2 = OneHotEncoder()
data_3 = data_cat.copy()
data_ohe = encoder.fit_transform(data_3).toarray()
```

*Output :*

```
array([[1., 0., 1., ..., 0., 0., 1.],
       [0., 1., 1., ..., 0., 1., 0.],
       [1., 0., 1., ..., 0., 0., 1.],
       ...,
       [1., 0., 1., ..., 0., 0., 1.],
       [0., 1., 1., ..., 0., 1., 0.],
       [1., 0., 1., ..., 1., 1., 0.]])
```

Berdasarkan output diatas data normalisasi masih berbentuk array. Oleh karena itu, masih susah untuk diartikan. Maka kita akan membuat data dalam bentuk dataframe dengan nama yang telah diberikan masing-masing kolom yaitu Pclass_1, Pclass_2, Pclass_3,dst. 

```
data_ohe = pd.DataFrame(data_ohe)
data_ohe = pd.DataFrame(data_ohe, columns=['Pclass_1','Pclass_2','Pclass_3','Sex_female','Sex_male','Embarked_C','Embarked_Q','Embarked_S'])
data_ohe.head()
```

*Output :*

| Pclass_1 | Pclass_2 | Pclass_3 | Sex_female | Sex_male | Embarked_C | Embarked_Q | Embarked_S |
|----------|----------|----------|------------|----------|------------|------------|------------|
| 0.0      | 0.0      | 1.0      | 0.0        | 1.0      | 0.0        | 0.0        | 1.0        |
| 1.0      | 0.0      | 0.0      | 1.0        | 0.0      | 1.0        | 0.0        | 0.0        |
| 0.0      | 0.0      | 1.0      | 1.0        | 0.0      | 0.0        | 0.0        | 1.0        |
| 1.0      | 0.0      | 0.0      | 1.0        | 0.0      | 0.0        | 0.0        | 1.0        |
| 0.0      | 0.0      | 1.0      | 0.0        | 1.0      | 0.0        | 0.0        | 1.0        |
