# 05 Intercept

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Pada video kali ini kita akan mencari nilai intercept dari data kita sebelumnya berdasarkan rumus pada video sebelumnya. 

```
e = (dt['Weight'].sum()*(dt['Height']**2).sum())
e
```

*Output :* 

77466375

```
f = (dt['Height'].sum())*((dt['Height']*dt['Height'].sum())
f
```

*Output :* 

>78337875


```
bb = (e-f)/(c-d)
```

*Output :* 


>-177.85714285714286


Didapatkan besarnya nilai intercept sebesar -177.85714285714286. Nah setlah kita telah mendapatkan nilai slope dan nilai intercept maka kita dapat membentuk formula modelnya dengan perintah 

```
print('Weight =', m, '* Height +',bb)
```

*Output :* 


>Weight = 1.4285714285714286 * Height + -177.85714285714286


Arti dari output diatas yaitu ketika kita mempunyai nilai tinggi badan maka kita kalikan terlebih dahulu 1.4285714285714286 setelah itu ditambah dengan -177.85714285714286, maka kita dapat nilai untuk berat badan dari formula diatas. 