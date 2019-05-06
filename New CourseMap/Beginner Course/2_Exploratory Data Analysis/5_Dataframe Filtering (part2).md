# 05 Dataframe Filtering *part2* 

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Explorasi data pada video ini menggunakan teknik yang mirip dengan sebelumnya, namun pada video kali ini kita akan menggunakan filtering pada data yang memiliki konsumsi lebih dari nilai tertentu.

>**How many countries in Europe who consume wine more than 100?**

Seperti pada filtering sebelumnya, perbedaannya adalah pada ini kita menggunakan filter continent **Europe** serta kolom **wine_servings** yang memiliki nilai **lebih dari 100**.

```
df[(df['continent'] == 'Europe') & (df['wine_servings'] > 100)]
```
*Output :*

| country        | beer_servings | spirit_servings | wine_servings | total_litres_of_pure_alcohol | continent |
|----------------|---------------|-----------------|---------------|------------------------------|-----------|
| Andorra        | 245           | 138             | 312           | 12.4                         | Europe    |
| Austria        | 279           | 75              | 191           | 9.7                          | Europe    |
| Belgium        | 295           | 84              | 212           | 10.5                         | Europe    |
| Croatia        | 230           | 87              | 254           | 10.2                         | Europe    |
| Cyprus         | 192           | 154             | 113           | 8.2                          | Europe    |
| Czech Republic | 361           | 170             | 134           | 11.8                         | Europe    |
| Denmark        | 224           | 81              | 278           | 10.4                         | Europe    |
| France         | 127           | 151             | 370           | 11.8                         | Europe    |
| Georgia        | 52            | 100             | 149           | 5.4                          | Europe    |
| Germany        | 346           | 117             | 175           | 11.3                         | Europe    |
| Greece         | 133           | 112             | 218           | 8.3                          | Europe    |
| Hungary        | 234           | 215             | 185           | 11.3                         | Europe    |
| Ireland        | 313           | 118             | 165           | 11.4                         | Europe    |
| Italy          | 85            | 42              | 237           | 6.5                          | Europe    |
| Luxembourg     | 236           | 133             | 271           | 11.4                         | Europe    |
| Malta          | 149           | 100             | 120           | 6.6                          | Europe    |
| Montenegro     | 31            | 114             | 128           | 4.9                          | Europe    |
| Netherlands    | 251           | 88              | 190           | 9.4                          | Europe    |
| Norway         | 169           | 71              | 129           | 6.7                          | Europe    |
| Portugal       | 194           | 67              | 339           | 11.0                         | Europe    |
| Romania        | 297           | 122             | 167           | 10.4                         | Europe    |
| Serbia         | 283           | 131             | 127           | 9.6                          | Europe    |
| Slovakia       | 196           | 293             | 116           | 11.4                         | Europe    |
| Slovenia       | 270           | 51              | 276           | 10.6                         | Europe    |
| Spain          | 284           | 157             | 112           | 10.0                         | Europe    |
| Sweden         | 152           | 60              | 186           | 7.2                          | Europe    |
| Switzerland    | 185           | 100             | 280           | 10.2                         | Europe    |
| United Kingdom | 219           | 126             | 195           | 10.4                         | Europe    |

Nah, untuk menghitung jumlah negaranya, kita tinggal menambahkan fungsi ```len()``` di luar dari table filtering yang telah kita buat di atas.

```
len(df[(df['continent'] == 'Europe') & (df['wine_servings'] > 100)])
```
*Output :*
```
28
```