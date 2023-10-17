Title: Caso de Estudio - Ames Housing
Date: 2023-10-14 10:20
Category: CasosdeEstudio
Tags: 'Casos de Estudio', 'Analisis de Datos', 'Python', 'RapidMiner'
Cover: https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/AmesHeader.png?raw=true

# Objetivo

El objetivo principal al utilizar este conjunto de datos es predecir el precio de venta de una vivienda en Ames en función de ciertas características dadas.

Esto es un problema de regresión, donde lo que se busca es encontrar una relación entre las características de entrada y el precio de venta de la casa.

# Entendimiento de los datos

En este dataset contamos con datos de venta de propiedades en Ames entre los años 2006 y 2010.

Los datos estan dividos en dos datasets, uno de training y uno de test.

## Variables

Se cuenta con 80 variables (23 nominales, 23 ordinales, 14 discretas, 20 continuas) las cuales son:

-   **Id**: Identificador de la casa vendida.

-   **MSSubClass**: Identifica el tipo de vivienda involucrada en la venta.

    -   20: 1 planta 1946 y más nuevas, todos los estilos.
    -   30: 1 planta 1945 y más antiguas.
    -   40: 1 planta con ático terminado de todas las edades.
    -   45: 1-1/2 plantas sin terminar de todas las edades.
    -   50: 1-1/2 plantas terminadas de todas las edades.
    -   60: 2 plantas 1946 y más nuevas.
    -   70: 2 plantas 1945 y más antiguas.
    -   75: 2-1/2 plantas de todas las edades.
    -   80: División o nivel múltiple.
    -   85: Vestíbulo dividido.
    -   90: Dúplex - Todos los estilos y edades.
    -   120: 1 planta PUD (Desarrollo de Unidad Planificada) - 1946 y más nuevas.
    -   150: 1-1/2 plantas PUD - Todas las edades.
    -   160: 2 plantas PUD - 1946 y más nuevas.
    -   180: PUD - Multinivel, incluye nivel dividido/vestíbulo.
    -   190: Conversión de 2 familias - Todos los estilos y edades.

-   **MSZoning**: Identifica la clasificación de zonificación general de la venta.

    -   A: Agricultura.
    -   C: Comercial.
    -   FV: Zona residencial en aldea flotante.
    -   I: Industrial.
    -   RH: Densidad residencial alta.
    -   RL: Densidad residencial baja.
    -   RP: Densidad residencial baja, parque.
    -   RM: Densidad residencial media.

-   **LotFrontage**: Longitud en pies lineales de la calle conectada a la propiedad.

-   **LotArea**: Tamaño del lote en pies cuadrados.

-   **Street**: Tipo de acceso a la propiedad.

    -   Grvl: Grava.
    -   Pave: Pavimentado.

-   **Alley**: Tipo de acceso al callejón a la propiedad.

    -   Grvl: Grava.
    -   Pave: Pavimentado.
    -   NA: Sin acceso al callejón.

-   **LotShape**: Forma general de la propiedad.

    -   Reg: Regular.
    -   IR1: Ligeramente irregular.
    -   IR2: Moderadamente irregular.
    -   IR3: Irregular.

-   **LandContour**: Plenitud de la propiedad.

    -   Lvl: Casi plano/nivel.
    -   Bnk: Pendiente rápida y significativa desde el nivel de la calle hasta el edificio.
    -   HLS: Ladera: Pendiente significativa de lado a lado.
    -   Low: Depresión.

-   **Utilities**: Tipo de servicios públicos disponibles.

    -   AllPub: Todos los servicios públicos (Electricidad, Gas, Agua y Alcantarillado).
    -   NoSewr: Electricidad, Gas y Agua (Fosa séptica).
    -   NoSeWa: Solo Electricidad y Gas.
    -   ELO: Solo Electricidad.

-   **LotConfig**: Configuración del lote.

    -   Inside: Lote interior.
    -   Corner: Lote en esquina.
    -   CulDSac: Cul-de-sac.
    -   FR2: Frente en 2 lados de la propiedad.
    -   FR3: Frente en 3 lados de la propiedad.

-   **LandSlope**: Pendiente de la propiedad.

    -   Gtl: Pendiente suave.
    -   Mod: Pendiente moderada.
    -   Sev: Pendiente severa.

-   **Neighborhood**: Ubicación física dentro de los límites de la ciudad de Ames.

    -   Blmngtn Bloomington Heights
    -   Blueste Bluestem
    -   BrDale Briardale
    -   BrkSide Brookside
    -   ClearCr Clear Creek
    -   CollgCr College Creek
    -   Crawfor Crawford
    -   Edwards Edwards
    -   Gilbert Gilbert
    -   IDOTRR Iowa DOT and Rail Road
    -   MeadowV Meadow Village
    -   Mitchel Mitchell
    -   Names North Ames
    -   NoRidge Northridge
    -   NPkVill Northpark Villa
    -   NridgHt Northridge Heights
    -   NWAmes Northwest Ames
    -   OldTown Old Town
    -   SWISU South & West of Iowa State University
    -   Sawyer Sawyer
    -   SawyerW Sawyer West
    -   Somerst Somerset
    -   StoneBr Stone Brook
    -   Timber Timberland
    -   Veenker Veenker

-   **Condition1**: Proximidad a varias condiciones.

    -   Artery Adyacente a una calle principal.
    -   Feedr Adyacente a una calle secundaria.
    -   Norm Normal
    -   RRNn A menos de 200 pies del ferrocarril norte-sur.
    -   RRAn Adyacente al ferrocarril norte-sur.
    -   PosN Cerca de una característica fuera del sitio positiva, como un parque o cinturón verde.
    -   PosA Adyacente a una característica fuera del sitio positiva.
    -   RRNe A menos de 200 pies del ferrocarril este-oeste.
    -   RRAe Adyacente al ferrocarril este-oeste.

-   **Condition2**: Proximidad a varias condiciones (si más de una está presente).

    -   Artery Adyacente a una calle principal.
    -   Feedr Adyacente a una calle secundaria.
    -   Norm Normal
    -   RRNn A menos de 200 pies del ferrocarril norte-sur.
    -   RRAn Adyacente al ferrocarril norte-sur.
    -   PosN Cerca de una característica fuera del sitio positiva, como un parque o cinturón verde.
    -   PosA Adyacente a una característica fuera del sitio positiva.
    -   RRNe A menos de 200 pies del ferrocarril este-oeste.
    -   RRAe Adyacente al ferrocarril este-oeste.

-   **BldgType**: Tipo de vivienda.

    -   1Fam: Unifamiliar.
    -   2FmCon: Conversión de dos familias; originalmente construida como vivienda unifamiliar.
    -   Duplx: Dúplex.
    -   TwnhsE: Unidad de esquina de casa adosada.
    -   TwnhsI: Unidad interior de casa adosada.

-   **HouseStyle**: Estilo de vivienda.

    -   1Story: Una planta
    -   1.5Fin: Una planta y media: segundo nivel terminado
    -   1.5Unf: Una planta y media: segundo nivel sin terminar
    -   2Story: Dos plantas
    -   2.5Fin: Dos plantas y media: segundo nivel terminado
    -   2.5Unf: Dos plantas y media: segundo nivel sin terminar
    -   SFoyer: Vestíbulo dividido
    -   SLvl: Nivel dividido

-   **OverallQual**: Califica el material y el acabado general de la casa.

    -   10: Muy Excelente
    -   9: Excelente
    -   8: Muy Bueno
    -   7: Bueno
    -   6: Por Encima del Promedio
    -   5: Promedio
    -   4: Por Debajo del Promedio
    -   3: Regular
    -   2: Malo
    -   1: Muy Malo

-   **OverallCond**: Califica la condición general de la casa.

    -   10: Muy Excelente
    -   9: Excelente
    -   8: Muy Bueno
    -   7: Bueno
    -   6: Por Encima del Promedio
    -   5: Promedio
    -   4: Por Debajo del Promedio
    -   3: Regular
    -   2: Malo
    -   1: Muy Malo

-   **YearBuilt**: Fecha original de construcción.

-   **YearRemodAdd**: Fecha de remodelación (igual que la fecha de construcción si no hay remodelación ni adiciones).

-   **RoofStyle**: Tipo de techo.

    -   Flat: Plano
    -   Gable: A dos aguas
    -   Gambrel: Gambrel (Granero)
    -   Hip: A cuatro aguas
    -   Mansard: Mansarda
    -   Shed: Cobertizo

-   **RoofMatl**: Material del techo.

    -   ClyTile: Teja de Barro o Arcilla
    -   CompShg: Teja Estándar (Compuesta)
    -   Membran: Membrana
    -   Metal: Metal
    -   Roll: Rollos
    -   Tar&Grv: Grava y Alquitrán
    -   WdShake: Tejas de Madera Rústica
    -   WdShngl: Tejas de Madera

-   **Exterior1st**: Revestimiento exterior de la casa.

    -   AsbShng: Tejas de Asbesto
    -   AsphShn: Tejas de Asfalto
    -   BrkComm: Ladrillo Común
    -   BrkFace: Ladrillo a la Vista
    -   CBlock: Bloque de Hormigón
    -   CemntBd: Tablero de Cemento
    -   HdBoard: Tablero Duro
    -   ImStucc: Estuco Imitación
    -   MetalSd: Revestimiento de Metal
    -   Other: Otro
    -   Plywood: Contrachapado
    -   PreCast: Hormigón Prefabricado
    -   Stone: Piedra
    -   Stucco: Estuco
    -   VinylSd: Revestimiento de Vinilo
    -   Wd Sdng: Revestimiento de Madera
    -   WdShing: Tejas de Madera

-   **Exterior2nd**: Revestimiento exterior de la casa (si hay más de un material).

    -   AsbShng: Tejas de Asbesto
    -   AsphShn: Tejas de Asfalto
    -   BrkComm: Ladrillo Común
    -   BrkFace: Ladrillo a la Vista
    -   CBlock: Bloque de Hormigón
    -   CemntBd: Tablero de Cemento
    -   HdBoard: Tablero Duro
    -   ImStucc: Estuco Imitación
    -   MetalSd: Revestimiento de Metal
    -   Other: Otro
    -   Plywood: Contrachapado
    -   PreCast: Hormigón Prefabricado
    -   Stone: Piedra
    -   Stucco: Estuco
    -   VinylSd: Revestimiento de Vinilo
    -   Wd Sdng: Revestimiento de Madera
    -   WdShing: Tejas de Madera

-   **MasVnrType**: Tipo de revestimiento de mampostería.

    -   BrkCmn: Ladrillo Común
    -   BrkFace: Ladrillo a la Vista
    -   CBlock: Bloque de Hormigón
    -   None: Ninguno
    -   Stone: Piedra

-   **MasVnrArea**: Área de revestimiento de mampostería en pies cuadrados.

-   **ExterQual**: Evalúa la calidad del material en el exterior.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Promedio/Típico
    -   Fa: Regular
    -   Po: Malo

-   **ExterCond**: Evalúa la condición actual del material en el exterior.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Promedio/Típico
    -   Fa: Regular
    -   Po: Malo

-   **Foundation**: Tipo de cimiento.

    -   BrkTil: Ladrillo y Teja
    -   CBlock: Bloque de Hormigón
    -   PConc: Concreto Vertido
    -   Slab: Losa
    -   Stone: Piedra
    -   Wood: Madera

-   **BsmtQual**: Evalúa la altura del sótano.

    -   Ex: Excelente (más de 100 pulgadas)
    -   Gd: Bueno (90-99 pulgadas)
    -   TA: Típico (80-89 pulgadas)
    -   Fa: Regular (70-79 pulgadas)
    -   Po: Malo (menos de 70 pulgadas)
    -   NA: Sin Sótano

-   **BsmtCond**: Evalúa la condición general del sótano.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Típico - se permite una ligera humedad
    -   Fa: Regular - humedad o alguna grieta o asentamiento
    -   Po: Malo - grietas severas, asentamiento o humedad
    -   NA: Sin sótano

-   **BsmtExposure**: Se refiere a las paredes del nivel del sótano o del jardín.

    -   Gd: Buena Exposición
    -   Av: Exposición Promedio (niveles divididos o vestíbulos generalmente califican como promedio o mejor)
    -   Mn: Exposición Mínima
    -   No: Sin Exposición
    -   NA: Sin Sótano

-   **BsmtFinType1**: Clasificación del área terminada del sótano.

    -   GLQ: Buenas Áreas de Vivienda
    -   ALQ: Áreas de Vivienda Promedio
    -   BLQ: Áreas de Vivienda Inferiores al Promedio
    -   Rec: Sala de Entretenimiento Promedio
    -   LwQ: Baja Calidad
    -   Unf: Sin Terminar
    -   NA: Sin Sótano

-   **BsmtFinSF1**: Área cuadrada terminada de tipo 1.

-   **BsmtFinType2**: Clasificación del área terminada del sótano (si hay varios tipos).

    -   GLQ: Buenas Áreas de Vivienda
    -   ALQ: Áreas de Vivienda Promedio
    -   BLQ: Áreas de Vivienda Inferiores al Promedio
    -   Rec: Sala de Entretenimiento Promedio
    -   LwQ: Baja Calidad
    -   Unf: Sin Terminar
    -   NA: Sin Sótano

-   **BsmtFinSF2**: Área cuadrada terminada de tipo 2.

-   **BsmtUnfSF**: Área cuadrada sin terminar del sótano.

-   **TotalBsmtSF**: Área total en pies cuadrados del sótano.

-   **Heating**: Tipo de calefacción.

    -   Floor: Calefacción por Suelo Radiante
    -   GasA: Calefacción de Aire Forzado a Gas
    -   GasW: Calefacción de Agua Caliente o Vapor a Gas
    -   Grav: Calefacción por Gravedad
    -   OthW: Calefacción de Agua Caliente o Vapor, no a Gas
    -   Wall: Calefacción por Pared

-   **HeatingQC**: Calidad y condición de la calefacción.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Promedio/Típico
    -   Fa: Regular
    -   Po: Malo

-   **CentralAir**: Aire acondicionado central.

    -   N: No.
    -   Y: Sí.

-   **Electrical**: Sistema eléctrico.

    -   SBrkr: Interruptores de Circuito Estándar y Cableado Romex
    -   FuseA: Caja de Fusibles de más de 60 Amperios y cableado Romex (Promedio)
    -   FuseF: Caja de Fusibles de 60 Amperios y cableado principalmente Romex (Regular)
    -   FuseP: Caja de Fusibles de 60 Amperios y cableado principalmente en tubo flexible (Malo)
    -   Mix: Sistema Eléctrico Mixto

-   **1stFlrSF**: Pies cuadrados del primer piso.

-   **2ndFlrSF**: Pies cuadrados del segundo piso.

-   **LowQualFinSF**: Pies cuadrados terminados de baja calidad (en todos los pisos).

-   **GrLivArea**: Pies cuadrados de área de estar sobre el nivel del suelo.

-   **BsmtFullBath**: Baños completos en el sótano.

-   **BsmtHalfBath**: Medios baños en el sótano.

-   **FullBath**: Baños completos por encima del nivel del suelo.

-   **HalfBath**: Medios baños por encima del nivel del suelo.

-   **Bedroom**: Dormitorios por encima del nivel del suelo (no incluye dormitorios del sótano).

-   **Kitchen**: Cocinas por encima del nivel del suelo.

-   **KitchenQual**: Calidad de la cocina.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Promedio/Típico
    -   Fa: Regular
    -   Po: Malo

-   **TotRmsAbvGrd**: Total de habitaciones por encima del nivel del suelo (no incluye baños).

-   **Functional**: Funcionalidad de la casa (se asume típica a menos que se indiquen deducciones).

    -   Typ: Funcionalidad Típica
    -   Min1: Deducciones Menores 1
    -   Min2: Deducciones Menores 2
    -   Mod: Deducciones Moderadas
    -   Maj1: Deducciones Mayores 1
    -   Maj2: Deducciones Mayores 2
    -   Sev: Severamente Dañado
    -   Sal: Solo para Salvamento

-   **Fireplaces**: Número de chimeneas.

-   **FireplaceQu**: Calidad de la chimenea.

    -   Ex: Excelente - Chimenea de mampostería excepcional
    -   Gd: Bueno - Chimenea de mampostería en el nivel principal
    -   TA: Promedio - Chimenea prefabricada en la sala de estar principal o chimenea de mampostería en el sótano
    -   Fa: Regular - Chimenea prefabricada en el sótano
    -   Po: Malo - Estufa Ben Franklin
    -   NA: Sin Chimenea

-   **GarageType**: Ubicación del garaje.

    -   2Types: Más de un tipo de garaje
    -   Attchd: Adjunto a la casa
    -   Basment: Garaje en el Sótano
    -   BuiltIn: Integrado (parte de la casa, típicamente con espacio arriba del garaje)
    -   CarPort: Cochera
    -   Detchd: Separado de la casa
    -   NA: Sin Garaje

-   **GarageYrBlt**: Año de construcción del garaje.

-   **GarageFinish**: Acabado interior del garaje.

    -   Fin: Terminado
    -   RFn: Terminado de forma áspera
    -   Unf: Sin terminar
    -   NA: Sin garaje

-   **GarageCars**: Tamaño del garaje en capacidad de automóviles.

-   **GarageArea**: Tamaño del garaje en pies cuadrados.

-   **GarageQual**: Calidad del garaje.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Típico/Normal
    -   Fa: Regular
    -   Po: Malo
    -   NA: Sin Garaje

-   **GarageCond**: Condición del garaje.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Típico/Normal
    -   Fa: Regular
    -   Po: Malo
    -   NA: Sin Garaje

-   **PavedDrive**: Entrada pavimentada.

    -   Y: Pavimentada.
    -   P: Pavimento parcial.
    -   N: Suciedad/grava.

-   **WoodDeckSF**: Área del deck de madera en pies cuadrados.

-   **OpenPorchSF**: Área del porche abierto en pies cuadrados.

-   **EnclosedPorch**: Área del porche cerrado en pies cuadrados.

-   **3SsnPorch**: Área del porche de tres estaciones en pies cuadrados.

-   **ScreenPorch**: Área del porche con pantalla en pies cuadrados.

-   **PoolArea**: Área de la piscina en pies cuadrados.

-   **PoolQC**: Calidad de la piscina.

    -   Ex: Excelente
    -   Gd: Bueno
    -   TA: Promedio/Típico
    -   Fa: Regular
    -   NA: Sin Piscina

-   **Fence**: Calidad de la cerca.

    -   GdPrv: Buena Privacidad
    -   MnPrv: Mínima Privacidad
    -   GdWo: Buena Madera
    -   MnWw: Mínima Madera/Alambre
    -   NA: Sin Cerca

-   **MiscFeature**: Característica diversa no cubierta en otras categorías.

    -   Elev: Ascensor
    -   Gar2: Segundo Garaje (si no está descrito en la sección de garaje)
    -   Othr: Otro
    -   Shed: Cobertizo (más de 100 pies cuadrados)
    -   TenC: Cancha de Tenis
    -   NA: Ninguno

-   **MiscVal**: Valor de la característica diversa en dólares.

-   **MoSold**: Mes de venta (MM).

-   **YrSold**: Año de venta (AAAA).

-   **SaleType**: Tipo de venta.

    -   WD: Escritura de Garantía - Convencional
    -   CWD: Escritura de Garantía - Pago en Efectivo
    -   VWD: Escritura de Garantía - Préstamo de VA
    -   New: Casa recién construida y vendida
    -   COD: Escritura de Oficial del Tribunal/Herencia
    -   Con: Contrato - Pago inicial del 15% y términos regulares
    -   ConLw: Contrato - Pago inicial bajo y bajo interés
    -   ConLI: Contrato - Bajo interés
    -   ConLD: Contrato - Pago inicial bajo
    -   Oth: Otro

-   **SaleCondition**: Condición de venta.
    -   Normal: Venta Normal
    -   Abnorml: Venta Anormal - comercio, ejecución hipotecaria, venta corta
    -   AdjLand: Compra de Terreno Adyacente
    -   Alloca: Asignación - dos propiedades vinculadas con escrituras separadas, típicamente un condominio con unidad de garaje
    -   Family: Venta entre miembros de la familia
    -   Partial: La vivienda no se completó en la última evaluación (asociada a viviendas nuevas)

## Variable Objetivo

Nuestra variable objetivo en este caso sera SalesPrice.
**SalesPrice**: Valor de venta de la vivienda en dolares.

## Tratamiento de Datos

Como primer paso lo que haremos es trabajar con el dataset de entrenamiento en RapidMiner.
Para trabajar con el dataset de entrenamiento en RapidMiner, el primer paso es importar los datos. Al hacerlo, es muy importante asegurarse de que todas las variables tengan el tipo adecuado para asi lograr un análisis preciso. Los tipos que encontramos son los siguientes:

-   **Binomial**: Utiliza este tipo cuando tengas una variable categórica que representa una elección entre dos categorías, es decir, una variable dicotómica.

-   **Polinomica**: Emplea este tipo cuando tengas una variable categórica que representa una elección entre más de dos categorías.

-   **Integer**: Selecciona este tipo cuando tengas una variable numérica que representa un número entero.

-   **Real**: Utiliza este tipo cuando tengas una variable numérica que representa un número real.

Ademas es importante poner la variable objetivo como label.

En el dataset de training contamos con 1460 casos.

### Datos faltantes

Al analizar los datos, nos encontramos con que hay datos faltantes en algunas variables.
Estas variables son:

-   **LotFrontage**: 259 datos faltantes.
-   **GarageYrBlt**: 81 datos faltantes.
-   **MasVnrArea**: 8 datos faltantes.

![Valores Faltantes](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/ValoresFaltantes.png?raw=true)

Es importante aclarar que en las variables categoricas se pueden encontrar valores como NA. Esto no significa que sean datos faltantes, sino que son categorias. Por ejemplo, en la variable _Bsmt Exposure_, NA significa que no tiene sotano, por lo que no es un dato faltante.

Para los datos faltantes lo que se puede hacer es sustituir estos por el promedio.

### Datos no necesarios

Excluiremos el atributo _Id_ ya que no aporta valor.

Como nuestro objetivo es predecir el precio de venta de una vivienda en Ames, no tiene mucho sentido tener datos que solo se conocen cuando la casa es vendida. Por lo tanto, vamos a excluir los siguientes atributos:

-   _MoSold_
-   _YrSold_
-   _SaleType_
-   _SaleCondition_

### Correlaciones

Otra tarea por hacer es analizar las correlaciones. Esto se calcula para variables numericas y variables ordinales.

Si filtramos por los atributos que tiene una correlacion mayor a 0.5 con _SalesPrice_, nos quedamos con los siguientes:

![Correlaciones](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/CorrelacionVariableObjetivo.png?raw=true)

Ademas vemos ciertas correlaciones entre atributos.

![Correlaciones](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/CorrelacionAtributos.png?raw=true)

Si tomamos 0.7 como umbral, podemos ver que hay ciertas variables que estan muy correlacionadas entre si. Por ejemplo, _GarageCars_ y _GarageArea_ tienen una correlacion de 0.88. Si lo pensamos esto tiene sentido ya que si yo tengo un mayor tamaño de garages, mas autos puedo entrar.
Ademas, _TotRmsAbvGrd_ tiene una correlacion de 0.83 con _GrLivArea_ y _1stFlrSF_ tiene una correlacion de 0.82 con _TotalBsmtSF_.

### Outliers y sesgos

Al estudiar los outliers de los atributos con alta correlacion con la variable objetivo podemos observar algunos outliers por ejemplo en _1stFlrSF_.

![1stFlrSF](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/1stFlrSF.png?raw=true)

Ademas, podemos ver que hay cierto sesgo en los datos. Un ejemplo de esto es _YearBuilt_, en el que se puede notar una clara distribucion hacia la derecha, indicandonos que la mayoria de las casas son mas nuevas.

![YearBuilt](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/YearBuilt.png?raw=true)

Para evitar esto lo que se puede hacer es eliminar los outliers y normalizar los datos antes de entrenar el modelo.

# Modelado

Para este caso de estudio lo que se mostrara sera una comparacion del modelado aplicando las tecnicas de tratamiento de datos mencionadas anteriormente y sin aplicarlas. El modelo a utilizar ser el de regresion lineal y se utilizara el dataset de entrenamiento.

Este dataset de entrenamiento se dividira en dos, uno para entrenar el modelo y otro para probarlo. Esta division se hara 70% para entrenamiento y 30% para prueba. Se podria utiliar cross validation, pero esto hacer que el proceso de entrenamiento se vuelva muy lento.

![Modelo](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Model.png?raw=true)

## Sin tratamiento de datos

root_mean_squared_error: 71285.561 +/- 0.000

## Con tratamiento de datos

root_mean_squared_error: 36253.778 +/- 0.000

# Resultados

Como se puede ver, al utlizar metodos de tratamiento de datos el RMSE nos da considerablemente mas bajo. Esto se debe a que al tomarnos el trabajo de analizar las correlaciones, eliminar los outliers, normalizar los datos el modelo puede aprender mejor.

# Archivos

-   [Dataset.rmp](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Dataset.rmp)
-   [Dataset.ipynb](https://github.com/gcabrera243/gcabrera243.github.io/blob/main/content/CE/Dataset.ipynb)
