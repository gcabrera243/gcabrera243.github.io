Title: TA2 - Algoritmos Lineales - Construcción modelo de Regresión Lineal - Housing
Date: 2023-09-03 10:20
Category: UT3
cover:
tags: 'TAs','TA2','UT3'

Los objetivos de este Trabajo de Aplicación son:

1. Identificar cuáles atributos, entre los varios disponibles,son necesarios para predecir con exactitud la mediana de precios de una casa 
2. Construir un modelo de regresión lineal múltiple para predecir la mediana de los precios utilizando los atributos más importantes 
3. Evaluar la exactitud del modelo para predecir nuevos ejemplos

# Problema

Predecir el precio de una vivienda a partir de su ubicacion y de algunos atributos.

#Datos
| Número | Atributo | Descripción |
| ------ | -------- | ----------- |
| 1 | CRIM | Tasa de crimen per capita por ciudad (real, 0,006-88,976) |
| 2 | ZN | Proporción de terreno residencial zonificado para lotes de más de 25,000 pies cuadrados (real, 0-100) |
| 3 | INDUS | Proporción de acres de negocios minoristas por ciudad (real, 0,460-27,740) |
| 4 | CHAS | Variable dummy Charles River (1 si limita con el río; 0 en caso contrario) (real, 0-1) |
| 5 | NOX | Concentración de óxidos nítricos (partes por 10 millones) (real, 0,385-0,871) |
| 6 | RM | Número medio de habitaciones por vivienda (real, 3,561-8,780) |
| 7 | AGE | Proporción de unidades ocupadas por propietarios construidas antes de 1940 (real, 2,900-100) |
| 8 | DIS | Distancias ponderadas a cinco centros de empleo de Boston (real, 1,130-12,127) |
| 9 | RAD | Índice de accesibilidad a carreteras radiales (real, 1-24) |
| 10 | TAX | Tasa de impuesto a la propiedad de valor total por $10,000 (real, 187-711) |
| 11 | PTRATIO | Ratio alumnos-maestro por localidad (real, 12,6-22) |
| 12 | B | 1000(Bk - 0,63)^2 donde Bk es la proporción de población negra por ciudad (real, 0,320-396,900) |
| 13 | LSTAT | Porcentaje de población de estatus bajo (real, 1,730-37,970) |

## Variable objetivo

-   **MEDV**: Mediana de valores de hogares ocupados por propietarios (en miles de dólares).

#Preparación de datos

Al analizar las estadisticas se detectan algunos posibles valores outliers en CHAS y en INDUS

Lo que deberemos hacer es en un principio es randomizar el orden de los datos (así cuando separemos las dos particiones, éstas serán estadísticamente similares).

Luego separaremos el dataset en un conjunto para entrenamiento y otro conjunto “no visto” de prueba. Para esto se usara el bloque Filter Examples de RapidMiner.
![process1](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/process1.png?raw=true)
![processvalidation](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/processvalidation.png?raw=true)

# Regresión Lineal

## ¿Qué parámetros podemos variar en el operador “Linear Regression”?

-   **Feature selection**: Determina el algoritmo de feature selection a utilizar durante la regresión.
-   **Eliminate colinear features**: Determina si el algoritmo debe intentar eliminar atributos correlaciones durante la regresión.
-   **Use bias**: Determina si se debería calcular el coeficiente independiente para el modelo.
    Ridge

## ¿Qué hace “feature selection”?

Filtra los atributos que participaran en la linear regression utilizando distintos algoritmos.

## ¿Cómo afectan “eliminate colinear features” y “use bias”?

Eliminate colinear features elimina los atributos que tienen relación colineal.

Use bias determina si tiene que calcular o no un parámetro independiente o interceptor.

# Ejecución e interpretación

## ¿cuáles no parecen ser muy significativos?

Sin feature selection: ZN,INDUS,NOX y AGE parecen no ser significativos.
squared_correlation (R2): 0.758
![SalidaLinearRegression](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/SalidaLinearRegression.png?raw=true)

Con feature selection: Al aplicar Greedy se eliminan los que parecían no ser significativos.
squared_correlation(R2): 0.752

![Greedy](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/Greedy.png?raw=true)

# Aplicación sobre datos “no vistos”

![process2](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/process2.png?raw=true)

Al mirar las estadisticas de residuals podemos decir que se esta logrando identificar de manera casi correcta la variable objetivo.

![residuals](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/residuals.png?raw=true)

# Archivos

-[UT3_TA2.rmp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/TAs/TA2/UT3_TA2.rmp)
