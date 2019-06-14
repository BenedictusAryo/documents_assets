# Part 16

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video kali ini kita akan membahas bagaimana caranya membuat tree yang lebih interactive. Dimana, syntax yang dibutuhkan hamir sama seperti pada video sebelumnya. Namun, ada beberapa syntax yang membedakan, untuk lebih jelasnya perhatikan syntax berikut. 
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
![Assets](https://www.dropbox.com/sh/zfpg3q89pe9hnia/AADVzLd2Zog4PXGkenqI2H_Da/4.png?dl=1)

Nah, untuk penjelasan lengkap terkait syntax diatas dapat dilihat pada video berikut ya.