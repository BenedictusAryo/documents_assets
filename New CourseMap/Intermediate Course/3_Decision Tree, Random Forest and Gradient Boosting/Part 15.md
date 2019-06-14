# Part 15

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya mem-visualisasikan tree atau pohonnya. Dimana, sebelum melakukan visualisasi, teman-teman harus sudah meng-install *graphviz* seperti yang telah di tutorialkan pada video sebelumnya. <br>
Hal pertama yang perlu dilakukan untuk visualisasi tree yaitu mengimport package sebagai berikut. 
```
from sklearn import tree
from sklearn.tree import export_graphviz
from IPython.display import SVG, display
from graphviz import Source
```
Selanjutnya, kita perlu mendefinisikan labelnya terlebih dahulu menggunakan syntax sebagai berikut.
```
labels = X.columns
graph = Source(tree.export_graphviz(model_dt,
out_file = None, feature_names = labels 
                , class_names = ['Free', 'Positive'
                , filled = True))

display(SVG(graph.pipe(format='svg')))
```
![Assets](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AADTRHTD1bynBTfGzww4rlnGa/3.png?dl=1)

Untuk penjelasan lengkapnya dapat dilihat pada video berikut ya.