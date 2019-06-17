# 4_2_Interactive Tree Model Visualization

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya membuat visualisasi tree model dengan interactive. Dimana, syntax yang dibutuhkan hampir sama seperti pada video sebelumnya. Namun, ada beberapa syntax yang membedakan, untuk lebih jelasnya perhatikan syntax berikut. 

```
# class labels
labels = X.Columns
def plot_tree(crit, split, depth, min_split, min_leaf=0.2)

        estimator = DecisionTreeClassifier(random_state = 45
        , criterion = crit
        , splitter = split
        , max_depth = depth
        , min_samples_split=min_split
        , min_samples_leaf=min_leaf)
        estimator.fit(X_train, y_train)

    graph = Source(tree.export_graphviz(estimator
    , out_file=None
    , feature_names=labels
    , class_names=['Free','Suspected']
    , filled = True))

    display(SVG(graph.pip=(format='svg')))

    return estimator

inter=interactive(plot_tree
, crit = ["gini","etropy"]
, split = ["best","random"]
, depth=[1,2,3,4]
, min_split=(1,100)
, min_leaf=(1,50))

display(inter)
```
![Assets](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Intermediate%20Course/3_Decision%20Tree%2C%20Random%20Forest%20and%20Gradient%20Boosting/assets/4.png)

Nah, untuk penjelasan lengkap terkait syntax diatas dapat dilihat pada video berikut ya.