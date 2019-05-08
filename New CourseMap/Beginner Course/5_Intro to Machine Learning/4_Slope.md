# 04 Slope

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan melanjutkan data sebelumnya. Kita mempunyai data berikut
```
dt
```
*Output :*

| Height | Weight |
|--------|--------|
| 150    | 40     |
| 160    | 50     |
| 170    | 60     |
| 175    | 65     |
| 165    | 55     |
| 155    | 45     |
| 180    | 90     |

Dari data diatas, mari kita coba untuk memasukkannya kedalam rumus slope dan intercept. Kita akan bahas slope terlebih dahulu

```
a = 7 * ((dt['Height']*dt['Weight']).sum())
a
```

*Output :* 

>474775

```
b = (dt['Height'].sum() * dt['Weight'].sum())
```

*Output :*

>467775

```
c = 7*(dt['Height']**2).sum()
c
```

*Output :*

>1338925

```
d = (dt['Height'].sum())**2
d
```

*Output :*

>1334025

```
m = (a-b)/(c-d)
m
```

*Output :*

>1.4285714285714286

Maka didapatkan nilai `m` sebesar **1.4285714285714286.**