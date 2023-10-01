Title: PD7 - Algoritmos Lineales - Análisis Discriminante Lineal
Date: 2023-09-03 10:20
Category: UT3
cover:
tags: 'PDs' , 'UT3', 'PD7'

El siguiente ejercicio es un tutorial para realizar clasificación a partir de un conjunto de datos, usando
Análisis Discriminante Lineal y la librería scikit-learn de Python.

# Proceso

Para comenzar deberemos importar las siguientes librerias:

    import matplotlib
    import matplotlib.pyplot as plt
    import pandas as pd
    from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
    from sklearn.linear_model import LogisticRegression
    from sklearn.metrics import confusion_matrix, classification_report
    from sklearn.model_selection import train_test_split
    from sklearn.preprocessing import LabelEncoder

Luego cargaremos el archivo de datos 'sample.csv' y mostraremos sus valores.
Para esto utilizaremos el codigo:
input_file = "sample.csv"
df = pd.read_csv(input_file, header=0)
print(df.values)
![Valores](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/Valores.png?raw=true)

Podemos graficar los datos utilizando la librería.

    colors = ("orange", "blue")
    plt.scatter(df['x'], df['y'], s=300, c=df['label'],
    cmap=matplotlib.colors.ListedColormap(colors))
    plt.show()

![Grafica](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/Grafica.png?raw=true)

A continuación Obtenemos a partir del dataset los datos y las clases.
Dividimos el conjunto de datos en 2, uno para entrenamiento y otro para prueba

    X = df[['x', 'y']].values
    y = df['label'].values
    train_X, test_X, train_y, test_y = train_test_split(X, y, test_size=0.25,random_state=0, shuffle=True)

Creamos el modelo de LDA y lo entrenamos.

    lda = LinearDiscriminantAnalysis()
    lda = lda.fit(train_X, train_y)

## Evaluación

Ahora podemos predecir las clases para los datos del conjunto de prueba y ver los resultados.
y_pred = lda.predict(test_X)
print("Predicted vs Expected")
print(y_pred)
print(test_y)

![PredictedVsExpected](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/PredictedVsExpected.png?raw=true)

Reporte:
![Report](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/Report.png?raw=true)

Matriz de confusion:

![Matrix](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/Matrix.png?raw=true)

# Archivos

-   [UT3_TA7PD.ipynb](https://github.com/gcabrera243/blob/main/content/UT3/PDs/PD7/UT3_TA7PD.ipynb)
