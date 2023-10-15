Title: TA3 - Procesamiento previo de los datos - Iris
Date: 2023-09-03 10:20
Category: UT2
tags: 'TAs', 'Iris', 'RapidMiner'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA3/Header.jpg?raw=true

En este articulo, trabajeremos con el dataset de Iris y lo modelaremos en RapidMiner.

# Iris

Predecir la especie de una flor de iris en función de cuatro atributos relacionados con las dimensiones de sus sépalos y pétalos. Se trata de un problema de clasificacion.

Se cuenta con 4 atributos numéricos para predecir la especie de iris:

sepal_length: Longitud del sépalo en centímetros.
sepal_width: Ancho del sépalo en centímetros.
petal_length: Longitud del pétalo en centímetros.
petal_width: Ancho del pétalo en centímetros.

![estadisticas_iris](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA3/estadisticas_iris.png?raw=true)

La variable objetivo es iris y puede tomar los valores "Iris setosa," "Iris versicolor," y "Iris virginica."

Al aplicar deteccion de outliers por distancia detectamos 10 outliers.

Al hacer la grafica podemos ver que hay 3 zonas claramente diferenciadas, representadas en los colores azul, verde y naranja. sin embargo las zonas verde y naranja tienen una parte de su área solapada, lo que dificultaría la clasificación.

También se puede notar una correlación bastante fuerte entre la longitud del pétalo y su ancho.

![scatter_plot](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA3/scatter_plot.png?raw=true)

## Archivos

-   [iris.rmp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA3/iris.rmp?raw=true)
