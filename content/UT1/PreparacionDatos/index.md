Title: Preparación de Datos
Date: 2023-09-03 10:20
Category: UT1
Tags: 'UT1','Machine Learning', 'Preparación de Datos', 'Aprendizaje Automatico'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/PreparacionDatos/Header.png?raw=true

# Preparación de Datos

La preparación de datos es una etapa fundamental en el proceso de desarrollo de modelos de Machine Learning. Es una parte del proceso que consume más tiempo y esfuerzo, pero es esencial para garantizar que los modelos produzcan resultados precisos y confiables.

A menudo, los datos rara vez están disponibles en la forma requerida por los algoritmos de Machine Learning.

Además, durante la preparación de datos nos pueden surgir dudas como:

-   ¿Qué sucede si los datos contienen errores o información incorrecta?
-   ¿Y si faltan datos importantes?

Estos problemas deben abordarse cuidadosamente para garantizar la calidad de los datos y, en última instancia, la efectividad de los modelos de Machine Learning.

## Datos Faltantes

Uno de los problemas mas comunes a los que nos enfrentamos al preparar los datos es la presencia de datos faltantes. Lo que se puede hacer en estos casos es o bien eliminarlos o bien reemplazarlos por un valor que tenga sentido (por ejemplo se podria utilizar el promedio para llenar esta datos faltante).

## Errores en datos

Los errores en los datos pueden incluir valores atípicos (outliers), incoherencias o información incorrecta.

Lo que se puede hacer para identificar es revisar manualmente los datos sospechosos o utilizar técnicas estadísticas para detectar valores atípicos.

## Conversion tipo de datos

La conversión de tipos de datos implica transformar variables de un tipo a otro, como por ejemplo convertir datos categóricos en numéricos. Esto es necesario para que los algoritmos de Machine Learning puedan trabajar con los datos de manera efectiva.

La elección de la técnica de conversión dependerá de la naturaleza de las variables y de las necesidades del modelo.

## Feature Selection

La selección de características implica identificar y retener las variables más relevantes para el problema que se está abordando, mientras se descartan las menos importantes. Esto puede ayudar a mejorar la eficiencia y el rendimiento de los modelos de Machine Learning, reduciendo la complejidad y el ruido en los datos.
