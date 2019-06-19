# 5_Optimized Tree Visualization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Setelah kita mengetahui performa dari _Decision Tree_, kita dapat memvisualisasikannya untuk melihat bentuk dari _tree_ itu sendiri secara visual. Visualisasi dilakukan dengan menggunakan _graphviz_.

Sebelumnya kita harus melakukan _import packages_ yang diperlukan dalam melakukan visualisasi _tree_

```
from sklearn.tree import export_graphviz
from sklearn import tree
from IPython.display import SVG
from graphviz import Source
from IPython.display import display
```

Untuk lebih detailnya, yuk simak penjelasan di dalam video.

Hasil dari visualisasi _tree_ menggunakan _grphviz_ akan mengeluarkan _output_ seperti gambar di bawah ini.

![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/5_Crossvalidation%20and%20Optimization/assets/dtree_render.png)
