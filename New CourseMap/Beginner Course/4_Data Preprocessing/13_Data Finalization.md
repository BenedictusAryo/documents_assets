# 13 Data Finalization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Kali ini kita akan membahas tentang Data Finalization. Nah, disini kita akan menggabungkan data yang kita telah transformasikan dan data target yaitu ```Survived```.  

```
data_fix = data_m.copy()
data_fix = data_fix.join(data_ohe)
data_fix = data_fix.join(df['Survived'])
data_fix.head()
```
*Output :*

| Age                 | SibSp | Parch | Fare                 | Pclassnew | Sexnew | Embarkednew | Survived |
|---------------------|-------|-------|----------------------|-----------|--------|-------------|----------|
| 0.2711736617240512  | 0.125 | 0.0   | 0.014151057562208049 | 2         | 1      | 2           | 0        |
| 0.4722292033174164  | 0.125 | 0.0   | 0.13913573538264068  | 0         | 0      | 0           | 1        |
| 0.32143754712239253 | 0.0   | 0.0   | 0.015468569817999833 | 2         | 0      | 2           | 1        |
| 0.4345312892686604  | 0.125 | 0.0   | 0.10364429745562033  | 0         | 0      | 2           | 1        |
| 0.4345312892686604  | 0.0   | 0.0   | 0.015712553569072387 | 2         | 1      | 2           | 0        |
