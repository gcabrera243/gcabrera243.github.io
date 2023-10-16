Title: Introducción al aprendizaje automático

Date: 2023-09-03 10:20
Category: UT1
Tags: 'UT1','Machine Learning', 'Definicion', 'Aprendizaje Automatico'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/Header.webp?raw=true

# ¿Que es la "Inteligencia Artificial"?

La Inteligencia Artificial se refiere a un campo de la informática que se enfoca en la creación de sistemas y programas capaces de realizar tareas que, si fueran realizadas por un ser humano, requerirían inteligencia. Estos sistemas pueden comprender, razonar, aprender, planificar y tomar decisiones. La IA busca desarrollar máquinas que puedan imitar la capacidad cognitiva humana y realizar tareas de manera autónoma.

# ¿Qué es “Machine Learning”?

El Aprendizaje Automático es una subdisciplina de la Inteligencia Artificial que se centra en el desarrollo de algoritmos y modelos que permiten a las computadoras aprender de los datos y mejorar su rendimiento en tareas específicas sin ser programadas explícitamente. En lugar de seguir reglas predefinidas, el aprendizaje automático utiliza la información contenida en los datos para adaptarse y tomar decisiones.

# Diferencia entre IA y ML

1. **Ámbito de aplicación:**

    - La IA abarca un campo amplio y multidisciplinario que incluye la creación de sistemas inteligentes que pueden realizar una variedad de tareas, como el procesamiento de lenguaje natural, la visión por computadora y la toma de decisiones.
    - El Aprendizaje Automático es una subárea de la IA que se centra en el desarrollo de modelos y algoritmos específicos para entrenar máquinas en tareas basadas en datos.

2. **Naturaleza del enfoque:**

    - La IA puede involucrar tanto sistemas basados en reglas (programación lógica) como sistemas basados en datos (aprendizaje automático).
    - El Aprendizaje Automático se centra principalmente en el uso de datos y algoritmos de aprendizaje para mejorar el rendimiento de las máquinas en tareas específicas.

3. **Requiere programación explícita:**

    - La IA no siempre requiere el aprendizaje a partir de datos. Puede involucrar la programación de reglas lógicas para realizar tareas específicas.
    - El Aprendizaje Automático se basa en datos y no requiere una programación explícita de reglas. Los modelos se ajustan automáticamente a partir de los datos de entrenamiento.

4. **Evolución y adaptación:**
    - La IA puede implicar sistemas que no necesariamente se adaptan y evolucionan con el tiempo sin una intervención manual constante.
    - El Aprendizaje Automático se caracteriza por la capacidad de las máquinas para aprender y adaptarse a medida que se les suministra más información, lo que permite una mejora continua en el rendimiento.

# Herramientas de Machine Learning

Investigando en la web, encontramos que existen muchas herramientas para realizar y ejecutar modelos de Machine Learning, algunos de ellos son:

-   R y Python con SciKitLearn
-   RapidMiner
-   Microsoft Azure ML Studio
-   Knime
-   Weka
-   Keras, TensorFlow, etc.

En este curso utilizaremos Python con SciKitLearn y RapidMiner.

## Python con SciKitLearn

![python](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/python.png?raw=true)

Python es un lenguaje de programación ampliamente utilizado en la ciencia de datos y el aprendizaje automático. SciKit-Learn, o scikit-learn, es una biblioteca de aprendizaje automático de código abierto en Python que proporciona una amplia variedad de algoritmos de aprendizaje automático y herramientas para la preparación y evaluación de datos. Es una de las bibliotecas más populares en la comunidad de aprendizaje automático de Python y se utiliza para tareas como clasificación, regresión, clustering y preprocesamiento de datos.

## RapidMiner

![RapidMiner](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/RapidMiner.png?raw=true)

RapidMiner es una plataforma de análisis de datos y aprendizaje automático que permite a las organizaciones realizar análisis avanzados y construir modelos de aprendizaje automático de manera eficiente. Proporciona una interfaz visual fácil de usar que permite a los usuarios, incluso sin experiencia en programación, realizar tareas como preparación de datos, modelado predictivo y evaluación de modelos. RapidMiner se utiliza en una variedad de industrias para tomar decisiones basadas en datos y automatizar procesos de análisis.

# Proceso CRISP-DM

![Crisp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/Crisp.png?raw=true)

El proceso CRISP-DM, que significa "CRoss-Industry Standard Process for Data Mining" (Proceso Estándar de Minería de Datos de la Industria Cruzada), es un enfoque estándar y ampliamente utilizado en la industria para llevar a cabo proyectos de minería de datos. Este proceso proporciona una estructura sistemática y ordenada para guiar a los profesionales a través de las diversas etapas de un proyecto de minería de datos. A continuación, se describen las fases del proceso CRISP-DM:

## Comprensión del Negocio (Business Understanding)

En esta etapa inicial, se trabaja en estrecha colaboración con los interesados del negocio para comprender los objetivos, requerimientos y el contexto en el que se aplicará la solución de minería de datos. Se definen los objetivos del proyecto y se establece un plan de trabajo.

## Comprensión de los Datos (Data Understanding)

En esta etapa, se reúnen los datos relevantes para el proyecto. Se realiza una exploración de los datos para comprender su estructura, calidad y posibles problemas. Esto implica la identificación de fuentes de datos, la recolección de datos y la realización de un análisis exploratorio.

## Preparación de los Datos (Data Preparation)

En esta fase, se preparan los datos para el modelado. Esto implica la limpieza de datos, la selección de variables relevantes, la transformación de datos y la creación de conjuntos de datos adecuados para el modelado. La calidad y preparación de los datos son cruciales para el éxito del proyecto.

## Modelado (Modeling)

En esta etapa, se seleccionan y se aplican técnicas de modelado de datos, como algoritmos de aprendizaje automático, para construir modelos predictivos. Se ajustan varios modelos y se evalúan para determinar cuál es el más adecuado para los objetivos del proyecto.

## Evaluación (Evaluation)

En esta fase, se evalúan los modelos construidos en términos de su rendimiento y su capacidad para cumplir los objetivos del negocio. Se utilizan métricas de evaluación para determinar la calidad del modelo y si cumple con los requisitos establecidos.

## Despliegue (Deployment)

Una vez que se ha seleccionado el modelo adecuado, se procede a su implementación en el entorno de producción. Esto puede implicar la integración del modelo en un sistema existente, la creación de una aplicación de minería de datos o la toma de decisiones basadas en el modelo.

El proceso CRISP-DM es iterativo, lo que significa que a menudo se revisan y repiten ciertas etapas a medida que se obtienen nuevos datos o se adquiere una comprensión más profunda del problema. Este enfoque estructurado ha demostrado ser valioso en proyectos de minería de datos, ya que ayuda a garantizar que los resultados sean relevantes para los objetivos del negocio y que se tomen decisiones informadas basadas en los datos.

# Tipos de Algoritmos y sus Aplicaciones

A continuacion se presenta un cheat sheet con los algoritmos mas utilizados en Machine Learning y sus aplicaciones.

![CheatSheet](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/UT1/CheatSheet.png?raw=true)
