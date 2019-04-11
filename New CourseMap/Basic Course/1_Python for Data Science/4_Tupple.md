# 04 Tuple

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**
Apabila teman-teman telah mempelajari *list*, teman-teman pasti tau bila inisiasi *list* menggunakan kurung siku **[ ]**. Nah jenis kontainer data yang akan kita pelajari di video kali ini, ialah *tuple*.
##### Contoh Tuple
Untuk menginisiasi tuple, kita menggunakan tanda kurung **( )** .
``` 
contoh_tuple = (1,2,3)
print(contoh_tuple)
```
*Output :*
```
(1,2,3)
```
##### Perbedaan dengan list
Lalu, apakah perbedaan antara list dan tuple ?<br>
List memiliki kemampuan untuk menambah anggota elemennya menggunakan perintah *append*.
```
contoh_list = [1, 2, 3] 
contoh_list.append(4) 
print(contoh_list)
```
*Output :*
```
[1, 2, 3, 4]
```
##### Tuple untuk kontainer data fix
Sedangkan tuple tidak demikian, tuple tidak memiliki kemampuan untuk menambah anggota elemennya.<br>
Karena memang fungsinya untuk menyimpan data dengan elemen yang tetap jumlahnya.