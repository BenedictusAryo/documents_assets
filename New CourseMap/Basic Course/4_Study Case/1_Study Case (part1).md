# 01 Study Case (part1)

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
_Dataset untuk Latihan pada Bab ini bisa di download di : [FIFA World Cup 2018.xlsx](https://drive.google.com/file/d/1HTWQi3pNk46uZee0BgMtlLfI0z3vjY-e/view?usp=sharing)_

Pada video kali ini merupakan studi kasus yang akan kita gunakan dari yang sudah kita pelajari pada Basic Class. 

Data yang akan digunakan yaitu **Fifa Word Cup Russia 2018**. Data terdiri dari 2 sheet yaitu sheet ```match statistics``` yang merupakan hasil-hasil pertandingan dengan berbagai macam statistik yang ada dan sheet ```countries``` yang merupakan data yang berisi nama negara serta kontinen tempat negara tersebut berasal. 

Nah, kita harus menggabungkan data dari sheet ```match statistics``` dan sheet ```countries```. 

Terlebih dahulu kita panggil package yang diperlukan

```
import pandas as pd
import numpy as np
```
Masukin data pada kedua sheet
```
data_match = pd.read_excel('data/FIFA World Cup 2018.xlsx', sheet_name='match_statistics')
data_cou = pd.read_excel('data/FIFA World Cup 2018.xlsx', sheet_name='countries')
```
Nah mari kita lihat data yang akan digunakan 
```
data_match.head()
```
*Output :* 

| Date       | Team         | Opponent     | Goal Scored | Ball Possession % | Attempts | On-Target | Off-Target | Blocked | Corners | Offsides | Free Kicks | Saves | Pass Accuracy % | Passes | Distance Covered (Kms) | Fouls Committed | Yellow Card | Yellow & Red | Red | Man of the Match | 1st Goal | Round       | PSO | Goals in PSO | Own goals | Own goal Time |
|------------|--------------|--------------|-------------|-------------------|----------|-----------|------------|---------|---------|----------|------------|-------|-----------------|--------|------------------------|-----------------|-------------|--------------|-----|------------------|----------|-------------|-----|--------------|-----------|---------------|
| 14-06-2018 | Russia       | Saudi Arabia | 5           | 40                | 13       | 7         | 3          | 3       | 6       | 3        | 11         | 0     | 78              | 306    | 118                    | 22              | 0           | 0            | 0   | Yes              | 12.0     | Group Stage | No  | 0            |           |               |
| 14-06-2018 | Saudi Arabia | Russia       | 0           | 60                | 6        | 0         | 3          | 3       | 2       | 1        | 25         | 2     | 86              | 511    | 105                    | 10              | 0           | 0            | 0   | No               |          | Group Stage | No  | 0            |           |               |
| 15-06-2018 | Egypt        | Uruguay      | 0           | 43                | 8        | 3         | 3          | 2       | 0       | 1        | 7          | 3     | 78              | 395    | 112                    | 12              | 2           | 0            | 0   | No               |          | Group Stage | No  | 0            |           |               |
| 15-06-2018 | Uruguay      | Egypt        | 1           | 57                | 14       | 4         | 6          | 4       | 5       | 1        | 13         | 3     | 86              | 589    | 111                    | 6               | 0           | 0            | 0   | Yes              | 89.0     | Group Stage | No  | 0            |           |               |
| 15-06-2018 | Morocco      | Iran         | 0           | 64                | 13       | 3         | 6          | 4       | 5       | 0        | 14         | 2     | 86              | 433    | 101                    | 22              | 1           | 0            | 0   | No               |          | Group Stage | No  | 0            | 1.0       | 90.0          |

Pada tabel diatas merupakan tabel untuk data pada sheet ```match statistics``` yang terdiri dari 27 variabel.
```
data_cou.head()
```
*Output :*

| Country   | Continent     |
|-----------|---------------|
| Argentina | South America |
| Australia | Asia          |
| Belgium   | Europe        |
| Brazil    | South America |
| Colombia  | South America |

Pada tabel diatas merupakan data pada sheet ```countries``` yang terdiri dari 2 variabel yaitu ```Country``` dan ```Continent```. 