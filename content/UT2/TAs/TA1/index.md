Title: TA1 - Procesamiento previo de los datos - Titanic
Date: 2023-09-03 10:20
Category: UT2
tags: 'TAs', 'Titanic', 'RapidMiner'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA1/Header.png?raw=true

En este articulo, investigaremos el dataset de titanic.

# Problema

Se busca predecir dado los datos que se conocen antes de embarcar, si la persona embarcada sobrevivirá o no.

# Atributos

Clase Objetivo
survived - Supervivencia (0 = No; 1 = Sí)

Atributos
| Atributo | Descripción |
|-----------|-------------------------------------------------------|
| pclass | Clase de Pasajero (1 = 1ra; 2 = 2da; 3 = 3ra) |
| name | Nombre |
| sex | Género |
| age | Edad |
| sibsp | Número de Hermanos/Cónyuges a Bordo |
| parch | Número de Padres/Hijos a Bordo |
| ticket | Número de Boleto |
| fare | Tarifa del Pasajero |
| cabin | Cabina |
| embarked | Puerto de Embarque (C = Cherbourg; Q = Queenstown; S = Southampton) |
| boat | Bote Salvavidas (si sobrevivió) |
| body | Número de Cuerpo (si no sobrevivió y el cuerpo fue recuperado) |

![atributos](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA1/Atributos.png?raw=true)

De estas estadísticas se puede ver que faltan:

-   264 Edades
-   2 Tarifa del Pasajero
-   1015 Cabinas
-   3 Puertos de embarque
-   824 botes salvavidas
    entre otros

# Tratamiento de los datos

El bote salvavidas y el numero de cuerpo no son atributos que nos sirvan porque no contamos con esta informacion a la hora de embarcar.
Cabinas tampoco nos sirve porque tiene muchisimos valores faltantes 1015 de 1310 posibles.
Para los datos faltantes lo que se hizo fue reemplazarlos utilizando el promedio.
Luego se normalizan todos los datos.

# Correlaciones

Modelando el problema obtenemos la siguiente matriz de correlacion.
![CorrelationMatrix](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA1/CorrelationMatrix.png?raw=true)

y los pesos son

![Weights](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA1/Weights.png?raw=true)

# Archivos

A continuacion se deja el proceso de RapidMiner

-   [TA1](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT2/TAs/TA1/TA1.rmp?raw=true)
