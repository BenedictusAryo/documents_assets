# 09 Standar Scaler

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
 Selanjutnya, masih metode pada Numerical Data Normalization yaitu Standar Scaler merupakan data akan di normalisasi dengan menggunakan distribusi normal. Biasanya data normalisasi standar scaler yaitu -1 sampai 2. 
 contoh :

     data_raw  = [  0  , 1000 , 2000, 3000, 4000]

     data_norm = [-1.27, -0.63, 0 , 0.63,  1.27 ]

```
from sklearn.preprocessing import StandartScaler
scaler2 = StandarScaler()
data_s = scaler2.fit_transform(data_num)
data_s
```
*Output :* <br>
| Age                   | SibSp                | Parch               | Fare                  |
|-----------------------|----------------------|---------------------|-----------------------|
| -0.5657364610748746   | 0.4327933656785018   | -0.4736736092984604 | -0.5024451714361923   |
| 0.6638610320657843    | 0.4327933656785018   | -0.4736736092984604 | 0.7868452935884461    |
| -0.2583370877897099   | -0.47454519624983954 | -0.4736736092984604 | -0.4888542575852486   |
| 0.4333115021019107    | 0.4327933656785018   | -0.4736736092984604 | 0.4207302360686478    |
| 0.4333115021019107    | -0.47454519624983954 | -0.4736736092984604 | -0.4863374216869257   |

Dari tabel diatas data telah dinormalisasi dengan menggunakan Standar Scaler. 