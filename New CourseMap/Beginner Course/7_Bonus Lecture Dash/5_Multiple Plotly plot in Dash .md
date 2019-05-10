# 5. Multiple Plot

![covervideo](http://bit.ly/makeaicovervideo)

#### **Description :**

Pada video sebelumnya kita telah mempelajari bagaimana membuat **plotly plot** didalam **dash**. Nah, pada video kali ini kita akan membahas bagaimana membuat **multiple plot** menggunakan plotly didalam dash.

Dalam membuat **multiple plot** didalam dash kita dapat menggunakan syntax sebagai berikut:

```
app.layout = html.Div(children=[
    html.H1(children='Dash Web App Plotting using Plotly',
    html.H2(children='Scatterplots'),
    dcc.Graph(id='scatterplot',figure=fig)])
```

![multi_trace](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/7_Bonus%20Lecture%20Dash/assets/multitrace.gif)

Nah, selain membuat dua trace dalam satu graph, kita juga bisa membuat multiple dash core components lho menggunakan syntax sebagai berikut:

```
app.layout = html.Div(children=[
    html.H1(children='Dash Web App Plotting using Plotly'),
    
    html.H2(children='Scatterplots'),
    dcc.Graph(id='scatterplot',figure=fig1),
    
    html.H2(children='Barplot Graph'),
    dcc.Graph(id='lineplot',figure=fig2)])
```

Sehingga hasilnya akan seperti ini :

![multiplot](https://github.com/BenedictusAryo/documents_assets/raw/master/New%20CourseMap/Beginner%20Course/7_Bonus%20Lecture%20Dash/assets/multiple%20dcc.gif)
