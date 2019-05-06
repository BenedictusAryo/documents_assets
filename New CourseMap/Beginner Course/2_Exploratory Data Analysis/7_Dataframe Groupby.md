# 07 Dataframe Groupby

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Setelah mempelajari tentang filtering, pada video kali ini, kita akan mempelajari tentang pivoting atau group by, kita akan mempelajarinya dengan menjawab pertanyaan ini:

> **How much average consumption for each continent?**

Pertanyaan di atas, tidak spesifik menunjuk pada negara ataupun benua tertentu. Bahkan juga tidak menunjukkan fitur tertentu apakah beer_servings, wine_servings dan lainnya. Untuk memjawab pertanyaan tersebut, kita dapat memanfaatkan fitur ```groupby``` pada pandas.

```
df.groupby('continent').mean()
```
*Output :*
| continent     | beer_servings      | spirit_servings    | wine_servings      | total_litres_of_pure_alcohol |
|---------------|--------------------|--------------------|--------------------|------------------------------|
| Africa        | 61.471698113207545 | 16.339622641509433 | 16.264150943396228 | 3.00754716981132             |
| Asia          | 37.04545454545455  | 60.84090909090909  | 9.068181818181818  | 2.1704545454545454           |
| Europe        | 193.77777777777777 | 132.55555555555554 | 142.22222222222223 | 8.617777777777777            |
| North America | 145.43478260869566 | 165.7391304347826  | 24.52173913043478  | 5.995652173913044            |
| Oceania       | 89.6875            | 58.4375            | 35.625             | 3.3812500000000005           |
| South America | 175.08333333333334 | 114.75             | 62.416666666666664 | 6.308333333333334            |

kita hendak mengelompokkan data berdasarkan kolom 'continent', maka kita gunakan perintah **groupby('continent')**. 
Sedangkan untuk memunculkan nilainya dengan function **mean()** pengelompokan yg kita lakukan berdasarkan nilai rata-rata.

Seperti yang telah kita pelajari sebelumnya, kita juga dapat menggunakan **sort values** untuk menyorting data groupby tersebut. Pada kasus ini, kita akan mengurutkan berdasarkan kolom **total_litres_of_pure_alcohol** dari yang terbesar.

```
continent_groupby = df.groupby('continent').mean()
continent_groupby.sort_values(by='total_litres_of_pure_alcohol', ascending=False)
```
*Output :*
| continent         | beer_servings      | spirit_servings    | wine_servings      | total_litres_of_pure_alcohol |
|-------------------|-------------------:|-------------------:|-------------------:|-----------------------------:|
| **Europe**        | 193.77777777777777 | 132.55555555555554 | 142.22222222222223 | 8.617777777777777            |
| **South America** | 175.08333333333334 | 114.75             | 62.416666666666664 | 6.308333333333334            |
| **North America** | 145.43478260869566 | 165.7391304347826  | 24.52173913043478  | 5.995652173913044            |
| **Oceania**       | 89.6875            | 58.4375            | 35.625             | 3.3812500000000005           |
| **Africa**        | 61.471698113207545 | 16.339622641509433 | 16.264150943396228 | 3.00754716981132             |
| **Asia**          | 37.04545454545455  | 60.84090909090909  | 9.068181818181818  | 2.1704545454545454           |

Sama seperti perintah sebelumnya, hanya pada kasus sorting value, kita menambahkan perintah **sort_values()** dengan menambahkan kolom mana yang hendak kita urutkan nilainya, kemudian karena kita hendak mengurutkan dari yang terbesar, maka kita menambahkan parameter **ascending=False**. 