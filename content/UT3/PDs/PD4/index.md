Title: PD4 - Algoritmos Lineales - Implementación en Python
Date: 2023-09-03 10:20
Category: UT3
cover:
tags: 'PDs','UT3','PD4'

El objetivo es entender como utilizar regresion logistica en python.

## Logisitic Regression

class LogisticRegression(LinearClassifierMixin, SparseCoefMixin, BaseEstimator):

En el caso multiclase, el algoritmo de entrenamiento utiliza uno contra resto (OvR)

esquema si la opción 'multi_class' está configurada en 'ovr' y utiliza la Pérdida de entropía

cruzada si la opción 'multi_class' está configurada en 'multinomial'.

penalty: Especifica la norma de la penalización. Puede ser 'l1', 'l2', 'elasticnet' o None
(ninguna penalización).

dual: Formulación dual o primal.

tol (tolerancia): Tolerancia para los criterios de detención.

C: Inverso de la fuerza de regularización.

fit_intercept: Especifica si se debe agregar una constante a la función de decisión.

intercept_scaling: Útil solo cuando se utiliza el solucionador 'liblinear' y fit_intercept está
configurado en True.

class_weight: Pesos asociados a las clases.

random_state: Utilizado cuando el solucionador es 'sag', 'saga' o 'liblinear' para barajar los
datos.

solver (solucionador): Algoritmo a utilizar en el problema de optimización.

max_iter: Número máximo de iteraciones para que los solucionadores converjan.

multi_class: Especifica cómo se maneja el problema multiclase.

verbose: Para los solucionadores 'liblinear' y 'lbfgs', establece la verbosidad.

warm_start: Cuando se establece en True, reutiliza la solución de la llamada anterior a fit.

n_jobs: Número de núcleos de CPU utilizados al paralelizar sobre las clases.

l1_ratio: El parámetro de mezcla Elastic-Net.

Atributos
classes\_: Lista de etiquetas de clases conocidas por el clasificador.

coef\_: Coeficiente de las características en la función de decisión.

intercept\_: Intercepto (sesgo) añadido a la función de decisión.

n*features_in*: Número de características vistas durante el ajuste.

feature*names_in*: Nombres de las características vistas durante el ajuste.

n*iter*: Número real de iteraciones para todas las clases.

## Carga de datos

Crear un archivo Python y agregar las dependencias necesarias.
Leer el dataset desde el archivo CSV utilizando la librería Pandas. Y ver como esta
compuesto
Obtener a partir del dataset los datos y las clases.

## Entrenamiento y testing

Dividir el conjunto de datos en 2, uno para entrenamiento y otro para prueba.
Crear el un modelo de LR y entrenarlo.

## Evaluación

Predecir las clases para los datos del conjunto de prueba y ver los resultados

![PredictedVsExpected](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/PDs/PD4/PredictedVsExpected.png?raw=true)

Probar el modelo y ver el reporte.
![Report](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/PDs/PD4/Report.png?raw=true)

Ver la matriz de confusión
![Matrix](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/PDs/PD4/Matrix.png?raw=true)

## Archivos

[UT3_TA4_PD_Ej4.ipynb](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT3/PDs/PD4/UT3_TA4_PD_Ej4.ipynb?raw=true)
