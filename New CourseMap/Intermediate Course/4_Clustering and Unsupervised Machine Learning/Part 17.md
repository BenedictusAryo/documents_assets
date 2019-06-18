# Part 17

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya telah dijelaskan bagaimana caranya membuat scatter untuk dendogram berdasarkan data yang dimiliki. Pada video kali ini kita akan membahas mengenai bagaimana caranya membuat suatu dendogram. Dalam hal ini yaitu dengan menggunakan ```linkage``` dengan syntax sebagai berikut.
```
linked = linkage(data, 'single')

labelList = range(1, 11)

plt.figure(figsize=(10, 7))
dendogram(linked, orientation='top', labels=labelList,
          distance_sort='descending' show_leaf_counts=True)

plt.show()
```
![Assets](https://www.dropbox.com/sh/ew6mjmoq0illzml/AACgpTErxcFa22o_VXIW3gxxa/11.png?dl=1)
