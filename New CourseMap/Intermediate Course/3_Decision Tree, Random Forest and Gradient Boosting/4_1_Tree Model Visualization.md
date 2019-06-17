# 4_1_Tree Model Visualization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya mem-visualisasikan tree atau pohonnya. Dimana, sebelum melakukan visualisasi, teman-teman harus sudah meng-install *graphviz* seperti yang telah di jelaskan pada tutorial di video sebelumnya. <br>
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

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/3_Decision%20Tree%2C%20Random%20Forest%20and%20Gradient%20Boosting/assets/3.png)

