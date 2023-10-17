Title: Caso de Estudio - Mushrooms
Date: 2023-10-15 10:20
Category: CasosdeEstudio
Tags: 'Casos de Estudio', 'Analisis de Datos', 'Python', 'RapidMiner'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Mushrooms/Header.jpg?raw=true

# Objetivo

El objetivo es determinar si un hongo es comestible (clase "e") o venenoso (clase "p") en función de varias características observadas de los hongos.

Las características incluyen atributos como la forma del sombrero, la superficie del sombrero, la coloración, la forma del tallo, la textura, el olor, la población y la temporada de crecimiento.

Se desea construir un modelo de clasificación capaz de clasificar de manera confiable los hongos en comestibles o venenosos.\

# Entendimiento de los datos

El dataset cuenta con 22 atributos, todos nominales. La variable objetivo es class (clase), que tiene dos valores posibles: e para comestible y p para venenoso.

# Datos en Formato Markdown

## cap-shape (Forma del sombrero)

-   bell (campana): b
-   conical (cónica): c
-   convex (convexa): x
-   flat (plana): f
-   knobbed (abotonada): k
-   sunken (hundida): s

## cap-surface (Superficie del sombrero)

-   fibrous (fibrosa): f
-   grooves (surcos): g
-   scaly (escamosa): y
-   smooth (lisa): s

## cap-color (Color del sombrero)

-   brown (marrón): n
-   buff (crema): b
-   cinnamon (canela): c
-   gray (gris): g
-   green (verde): r
-   pink (rosa): p
-   purple (púrpura): u
-   red (rojo): e
-   white (blanco): w
-   yellow (amarillo): y

## bruises? (¿Tiene moretones?)

-   bruises (con moretones): t
-   no (sin moretones): f

## odor (Olor)

-   almond (almendras): a
-   anise (anís): l
-   creosote (creosota): c
-   fishy (a pescado): y
-   foul (fétido): f
-   musty (a humedad): m
-   none (ninguno): n
-   pungent (acre): p
-   spicy (picante): s

## gill-attachment (Tipo de sujeción de las branquias)

-   attached (adjunta): a
-   descending (descendente): d
-   free (libre): f
-   notched (encajada): n

## gill-spacing (Espaciado entre las branquias)

-   close (cercano): c
-   crowded (abigarrado): w
-   distant (distante): d

## gill-size (Tamaño de las branquias)

-   broad (ancho): b
-   narrow (estrecho): n

## gill-color (Color de las branquias)

-   black (negro): k
-   brown (marrón): n
-   buff (crema): b
-   chocolate (chocolate): h
-   gray (gris): g
-   green (verde): r
-   orange (naranja): o
-   pink (rosa): p
-   purple (púrpura): u
-   red (rojo): e
-   white (blanco): w
-   yellow (amarillo): y

## stalk-shape (Forma del tallo)

-   enlarging (en agrandamiento): e
-   tapering (en estrechamiento): t

## stalk-root (Raíz del tallo)

-   bulbous (bulbosa): b
-   club (club): c
-   cup (taza): u
-   equal (igual): e
-   rhizomorphs (rizomorfos): z
-   rooted (enraizada): r
-   missing (desconocida): ?

## stalk-surface-above-ring (Superficie del tallo (arriba del anillo))

-   fibrous (fibrosa): f
-   scaly (escamosa): y
-   silky (seda): k
-   smooth (lisa): s

## stalk-surface-below-ring (Superficie del tallo (abajo del anillo))

-   fibrous (fibrosa): f
-   scaly (escamosa): y
-   silky (seda): k
-   smooth (lisa): s

## stalk-color-above-ring (Color del tallo (arriba del anillo))

-   brown (marrón): n
-   buff (crema): b
-   cinnamon (canela): c
-   gray (gris): g
-   orange (naranja): o
-   pink (rosa): p
-   red (rojo): e
-   white (blanco): w
-   yellow (amarillo): y

## stalk-color-below-ring (Color del tallo (abajo del anillo))

-   brown (marrón): n
-   buff (crema): b
-   cinnamon (canela): c
-   gray (gris): g
-   orange (naranja): o
-   pink (rosa): p
-   red (rojo): e
-   white (blanco): w
-   yellow (amarillo): y

## veil-type (Tipo de velo)

-   partial (parcial): p
-   universal (universal): u

## veil-color (Color del velo)

-   brown (marrón): n
-   orange (naranja): o
-   white (blanco): w
-   yellow (amarillo): y

## ring-number (Número de anillos)

-   none (ninguno): n
-   one (uno): o
-   two (dos): t

## ring-type (Tipo de anillo)

-   cobwebby (en tela de araña): c
-   evanescent (evanescente): e
-   flaring (en expansión): f
-   large (grande): l
-   none (ninguno): n
-   pendant (colgante): p
-   sheathing (envuelto): s
-   zone (en zona): z

## spore-print-color (Color de la impresión de esporas)

-   black (negro): k
-   brown (marrón): n
-   buff (crema): b
-   chocolate (chocolate): h
-   green (verde): r
-   orange (naranja): o
-   purple (púrpura): u
-   white (blanco): w
-   yellow (amarillo): y

## population (Población)

-   abundant (abundante): a
-   clustered (aglomerada): c
-   numerous (numerosa): n
-   scattered (dispersa): s
-   several (varias): v
-   solitary (solitaria): y

## habitat (Hábitat)

-   grasses (praderas): g
-   leaves (hojas): l
-   meadows (prados): m
-   paths (caminos): p
-   urban (urbano): u
-   waste (residuos): w
-   woods (bosques): d

# Datos faltantes

Al analizar los datos, nos encontramos con que hay datos faltantes en la variable _stalk-root_. Tenemos un total de 2480 sin categoria definida.

Se podria eliminar todas las filas que tiene missings pero eso seria eliminar alrededor de un 30% del dataset. Se opta por imputar los valores faltantes por la moda.

# Modelado

Se modelara el problema utilizando Naive Bayes y LDA. Compararemos su performance y elegiremos el mejor modelo.

El model en RapidMiner queda de la siguiente manera:

![Model](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Mushrooms/Model.png?raw=true)

# Evaluación

Performance Naive Bayes:

![NaiveBayes](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Mushrooms/NaiveBayes.png?raw=true)

Performance LDA:

![LDA](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Mushrooms/LDA.png?raw=true)

# Conclusion

Se puede concluir que el mejor modelo es el de Naive Bayes, ya que tiene un mejor performance en la clasificación de los hongos. Esta performance es de 99.57% de accuracy.

# Archivos

-   [Mushrooms.rmp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Mushrooms/Mushrooms.rmp)
