Title: TA2 - Procesamiento previo de los datos - Wine
Date: 2023-09-03 10:20
Category: UT2
cover:
tags: ['TAs']

En este artículo, utilizaremos el conjunto de datos Wine de la UCI como ejemplo práctico para demostrar lo aprendido de normalizacion.

# Problema

Problema planteado: Determinar la clase de vino a partir de sus concentraciones de varios nutrientes. Se trata de un problema de clasificacion donde vamos a tener 3 clases.

# Atributos

Variable objetivo: class (clase de vino) que es de tipo categórico

![atributos](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA2/atributos.jpg?raw=true)

Se detectaron 10 outliers en los datos.
![outliers](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA2/Outliers.png?raw=true)

# Canales

Se crearon dos canales, uno donde se utiliza el dataset tal cual esta y otro en donde se aplican bloques para normalizar y estandarizar los datos.

Para el dataset sin bloques:
![performance](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA2/PerformanceSinNormalizar.png?raw=true)

Para el dataset con bloques:
![performance](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA2/PerformanceNormalizado.png?raw=true)

Dio mejor la performance de los datos sin normalizar en este caso. Esto puede ser por el split actual de datos.

# Archivos

[UT2_PD1_Ej2.rmp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/UT2_PD1_Ej2.rmp?raw=true)
