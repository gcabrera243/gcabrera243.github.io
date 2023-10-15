Title: PD4 - Análisis del dataset “Titanic” con python
Date: 2023-09-03 10:20
Category: UT2
tags: 'PDs', 'Titanic', 'Python'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/Header.png?raw=true

En este ejercicio se desea construir un modelo de predicción para el dataset “Titanic”, utilizando
Python y sklearn.

## Importar Librerias

Lo primero que hacemos es importar las librerias que van a ser necesarias para el desarrollo del modelado

    import numpy as np
    import pandas as pd
    from sklearn.preprocessing import LabelEncoder
    from sklearn.model_selection import train_test_split
    import seaborn as sns
    from matplotlib import pyplot as plt
    sns.set_style("whitegrid")
    %matplotlib inline
    import warnings
    warnings.filterwarnings("ignore")

## Cargar Datos

Con Panda cargamos los datos de entrenamiento y test. Con head() podremos visualizar una muestra de los datos.

    training = pd.read_csv("train.csv")
    testing = pd.read_csv("test.csv")
    training.head()

![training](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/training.png?raw=true)

    testing.head()

![testing](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/testing.png?raw=true)

## Valores NaN

Debemos reemplazar la data faltante.

    def null_table(training, testing):
    print("Training Data Frame")
    print(pd.isnull(training).sum())
    print(" ")
    print("Testing Data Frame")
    print(pd.isnull(testing).sum())

    null_table(training, testing)

![dataFaltante](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/dataFaltante.png?raw=true)

Nos deshacemos de la columna Cabin

    training.drop(labels = ["Cabin", "Ticket"], axis = 1, inplace = True)
    testing.drop(labels = ["Cabin", "Ticket"], axis = 1, inplace = True)

    null_table(training, testing)

Y para Age, Embarked y Fare los reemplazamos por su mediana

    training["Age"].fillna(training["Age"].median(), inplace = True)
    testing["Age"].fillna(testing["Age"].median(), inplace = True)
    training["Embarked"].fillna("S", inplace = True)
    testing["Fare"].fillna(testing["Fare"].median(), inplace = True)

    null_table(training, testing)

![dataCompleta](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/dataCompleta.png?raw=true)

## Visualizacion

### Genero

![Genero](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/barPlot.png?raw=true)

### Clase

![Clase](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/pClass.png?raw=true)

![SurvivalRate](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/SurvivalRate.png?raw=true)

![SurvivalRates2](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/SurvivalRates2.png?raw=true)

## Codigo implementado

-   [codigo](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/PDs/PD4/UT2_PD4.ipynb?raw=true)
