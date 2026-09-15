# Unidad 3. Medidas de Resumen - Práctica

```{rubric} Datasets
:class: rubric-datasets
```

| Dataset | Ejercicio/s | Descripción |
|---|---|---|
| [`winequality-red.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/winequality-red.csv) | 1 | Propiedades fisicoquímicas de una muestra de vinos tintos junto con el puntaje de calidad asignado por un panel de enólogos. |
| [`alimentos.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/alimentos.csv) | 2 | Listado de alimentos permitidos en un plan de dieta, con su aporte calórico, tipo de alimento y vitamina que aportan. |
| [`pacientes.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/pacientes.csv) | 2 y 4 | Planilla de seguimiento de 50 pacientes de una clínica de nutrición, con peso inicial, peso final, altura, sexo y tiempo de tratamiento. |
| [`titanic.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/titanic.csv) | 3 | Listado de pasajeros del Titanic con variables sociodemográficas, clase, tarifa y condición de supervivencia, ampliado con datos de Wikipedia. |
| [`wine_quality.xlsx`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/wine_quality.xlsx) | 5 | Puntuaciones organolépticas (claridad, aroma, cuerpo, sabor y calidad general) asignadas por un panel de enólogos a 76 vinos Pinot Noir. |
| [`wine_aging.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/wine_aging.csv) | 5 | Tabla de referencia con el grado de envejecimiento (crianza, reserva, gran reserva) de cada vino de `wine_quality.xlsx`. |
| [`calidad_producto.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/calidad_producto.csv) | 6 | Registros de control de calidad industrial con la desviación de largo respecto a un valor estándar y un índice de calidad del producto. |
| [`estacion_meteorologica.csv`](https://raw.githubusercontent.com/tuiafceiaunr/fdcd/main/unidades/u3-analisis-exploratorio-datos/datasets/estacion_meteorologica.csv) | 7 | Registros de una estación meteorológica con variables ambientales (temperatura, humedad, viento, radiación solar, presión, etc.) medidas a lo largo del tiempo. |

```{rubric} Ejercicio 1
:class: rubric-ejercicio
```

El dataset **`winequality-red.csv`** contiene un conjunto de variables relacionadas con propiedades fisicoquímicas que fueron determinadas sobre una serie de vinos de una misma variedad, así como un puntaje asignado en cada caso por un panel de enólogos en sesiones de cata. Importe el dataset al entorno de trabajo y realice cualquier tipo de limpieza y adecuación del mismo que considere necesaria para su posterior análisis.

a) Clasifique las variables del dataset en cualitativas, cuantitativas discretas y cuantitativas continuas.

b) El 25% de los vinos del dataset tiene un contenido de alcohol superior a… ¿qué valor?

c) Realice una tabla en la que se presenten, para las variables densidad y pH, **únicamente** las siguientes medidas descriptivas: media, mediana, desvío estándar y rango intercuartil. A continuación, responda a las siguientes preguntas **sin realizar ningún gráfico:**

- ¿Cómo describiría ambas distribuciones en relación a sus características de simetría?
- ¿Cuál de los dos conjuntos de observaciones (densidad o pH) presenta mayor variabilidad?

d) Represente la distribución de las observaciones de la variable contenido de alcohol (alcohol) a través de un boxplot. *Sugerencia*: utilice la función `sns.boxplot()` de la librería  `seaborn`. Basándose en el gráfico, ¿cuál de las siguientes medidas de posición o centralidad (media aritmética/mediana) le parece más adecuada para describir a esta variable?

e) Realice una tabla de frecuencias para resumir la distribución de los vinos del dataset en función del puntaje asignado según su calidad (`quality`).

- ¿Cuál de los puntajes fue recibido por una mayor cantidad de vinos?
- ¿Qué porcentaje de los vinos de la muestra recibieron la calificación más baja?


```{rubric} Ejercicio 2
:class: rubric-ejercicio
```

El dataset **`alimentos.csv`** fue elaborado por una clínica de nutrición que suministró a sus pacientes una lista de alimentos permitidos con sus respectivos contenidos calóricos. También se detalló el tipo de alimento del que se trataba (fruta, verdura, etc.) y el tipo de vitamina que aportaba cada uno (A, B o C).

Por otra parte, la nutricionista a cargo del estudio lleva una planilla de control de la evolución de 50 pacientes (**`pacientes.csv`**) en la que registra el sexo, la altura, el peso inicial y el peso final de cada uno de ellos luego de seguir un plan de dieta por una cierta cantidad de tiempo, información que también fue registrada en el campo `tiempo_tratamiento_dias`.

a) Importe ambos datasets al entorno de trabajo y realice cualquier tarea de limpieza y/o adecuación de los mismos que considere necesaria.

b) En relación al campo `aporte_calorico_kcal` informe las medidas descriptivas que le brinden información sobre los siguientes aspectos:

- Las kcal que aportan, en promedio, los alimentos que forman parte del dataset.
- Aquel valor de aporte calórico tal que el 50% de los alimentos del dataset presentan aportes calóricos menores o iguales a él.
- La dispersión o variabilidad del 50% central de las observaciones.
- El o los valores que se presentan con mayor frecuencia entre las observaciones.

c) Represente la distribución de las observaciones de la variable `aporte_calorico_kcal` a través de un boxplot.

- Identifique en el gráfico la mediana, el primer y el tercer cuartil.
- ¿Cómo caracterizaría a la distribución en relación a sus características de simetría?
- En función a lo observado, ¿qué par de medidas de centralidad/posición (media aritmética - mediana) y de dispersión (rango intercuartil - rango - desviación estándar) le parece más adecuada para describir a este conjunto?
- ¿Existe alguna observación que pueda ser considerada como atípica? En caso de respuesta afirmativa, ¿cuántas observaciones recibirían esta calificación?

d) ¿Qué tipo de alimento presenta la mayor mediana de aporte calórico?

e) Realice un boxplot para representar la distribución de los aportes calóricos de alimentos de los siguientes tipos: frutas, verduras y alimentos elaborados.
- ¿Qué tipo de alimentos presenta valores calóricos más variables y cuál menos variables?
- ¿Qué medida descriptiva utilizó para responder a estas últimas preguntas?

f) Utilizando los datos de los/las pacientes, genere una variable que corresponda a la variación de peso para cada paciente a lo largo del tratamiento (`peso_final_kg` - `peso_inicial_kg`).

- Represente los valores observados de la variable “diferencia de peso” en función del sexo a través de un boxplot.
- ¿Qué medida descriptiva utilizaría para comparar los resultados del tratamiento entre personas de ambos sexos? En función de su respuesta, ¿las personas de qué sexo obtuvieron los mejores resultados para el tratamiento?

```{rubric} Ejercicio 3
:class: rubric-ejercicio
```

Importe y explore el conjunto de datos **`titanic.csv`**.

a) Realice una descripción general del conjunto de datos que incluya la descripción de la información brindada por cada columna, el tipo de datos que contiene cada una y el número de registros.

b) La columna `Survived` presenta valores faltantes para una parte de los registros. **A partir de este punto, trabaje únicamente con aquellas observaciones para las que se conoce si el/la pasajero/a sobrevivió o no.**

c) 

- Calcule la media, la mediana y la desviación estándar de la edad de los/las pasajeros/as que murieron y sobrevivieron para cada clase. 

- Realice un boxplot que muestre la distribución de edades para cada grupo (murieron/sobrevivieron) dentro de cada clase. ¿En qué clase las edades de las personas que sobrevivieron fueron más variables? ¿Cuál fue la edad de la persona más joven que sobrevivió en tercera clase?

d) Represente gráficamente la distribución de los precios de los pasajes en función de la clase del pasajero y calcule el promedio, la moda, la mediana, la desviación estándar y el rango intercuartil del precio del pasaje para cada grupo. ¿En qué clase los precios de pasaje presentaron una mayor variabilidad?

e)

- ¿Qué medida resumen calcularía si quisiera conocer aquel valor que representa el precio que sólo el 25% de los pasajeros superaron a la hora de comprar su boleto? 
    
- Identifique cuáles fueron los pasajeros que pagaron un pasaje igual o más caro que el valor calculado en el ítem anterior. Construya una tabla en la que se informen los nombres de estas personas, el número total de personas vinculadas a ellas que se encontraban en el barco y la ciudad en la que embarcaron.
    
- En base a la tabla construida en el ítem anterior, ¿con cuántos acompañantes, en promedio, viajaban estos pasajeros? ¿En qué puerto embarcó la mayoría de ellos?
    
f) Construya una tabla en la que se resuma la distribución de pasajeros del Titanic en función de la clase en la que viajaron. La misma debe contener la siguiente información (en distintas columnas): cantidad de pasajeros/as que viajaron en cada clase y porcentajes en relación al total. ¿A qué clase pertenecía la mayoría de los pasajeros del Titanic?

g) Construya una tabla de contingencia cruzando las variables `survived` y `Pclass`. ¿Qué proporción de personas de cada clase sobrevivieron al naufragio del Titanic? Represente gráficamente esta información en un gráfico de barras.

```{rubric} Ejercicio 4
:class: rubric-ejercicio
```

Teniendo en cuenta la variable `altura_m` que se encuentra en el dataset `pacientes.csv` trabajado en el **Ejercicio 2**, genere una tabla de frecuencias en la que las observaciones se encuentren segmentadas en subintervalos de 10 cm de amplitud que estén “cerrados por izquierda”, es decir, que tengan la forma **[extremo_inferior, extremo_superior)**.

La tabla de frecuencias generada deberá contener columnas en las que se especifiquen las frecuencias absolutas, relativas y relativas acumuladas correspondientes a cada subintervalo.
¿Qué porcentaje de las personas del dataset tienen una altura **menor a 1.8 m**?

```{rubric} Ejercicio 5
:class: rubric-ejercicio
```

El dataset **`wine_quality.xlsx`** contiene información acerca del puntaje que un panel de enólogos
asignó a una serie de 76 vinos de tipo Pinot Noir. Las cualidades evaluadas incluyeron algunas
propiedades organolépticas como claridad (*clarity*), aroma (*aroma*), cuerpo (*body*) y sabor (*flavor*) y una valoración de la calidad general del vino (*quality*). Adicionalmente, se recabó información sobre el grado de envejecimiento (*aging*) de cada uno de los productos evaluados, la cual se encuentra en el dataset `wine_aging.csv`.

a) Importe ambos datasets y realice cualquier tarea de limpieza y adecuación de los mismos que
considere necesaria para su posterior análisis.

b) ¿Cuál es el tipo de vino (crianza/reserva/gran reserva) que presenta la mayor mediana para el sabor?

c) Construya la matriz de covariancia de las distintas variables cuantitativas que componen el
dataset y comente qué tipo de información le aporta acerca de la relación entre los distintos
pares de variables cuantitativas del dataset.

d) Construya la matriz de correlación de las distintas variables cuantitativas que componen el
dataset. En base al mismo, identifique la/s variable/s que se encuentran más fuertemente
correlacionadas e informe e interprete la medida de asociación lineal correspondiente

e) Elija el par de variables que identificó en el ítem anterior como aquellas que se encuentran más fuertemente correlacionadas linealmente y realice un gráfico que le permita visualizar la relación general que existe entre las mismas.

```{rubric} Ejercicio 6
:class: rubric-ejercicio
```

Utilizando el dataset `calidad_producto.csv`, que contiene dos variables registradas en el área de control de calidad de una industria:

- `desviacion_largo`: desviación del largo del producto respecto a un valor estándar o deseado.
- `indice_calidad_producto`: índice o puntuación que se construye a partir de una serie de
aspectos relacionados a la calidad general del producto.

a) Calcule los coeficientes de correlación de Pearson y Spearman entre ambas variables. Interprete los valores obtenidos en relación al tipo de información que le brinda cada uno acerca del grado de asociación entre las variables.

b) Construya un gráfico que le permita visualizar la relación general que existe entre las variables analizadas. ¿Qué observa?

c) Calcule nuevamente ambos coeficientes sin tomar en cuenta los registros que incluyan
observaciones potencialmente atípicas. ¿Cómo resultan los valores obtenidos en comparación
con los calculados en el ítem 1?

d) En función de las características de la relación entre ambas variables que se observan
gráficamente, ¿cuál de las dos métricas informaría para describir en forma cuantitativa el grado de asociación entre ellas?

```{rubric} Ejercicio 7
:class: rubric-ejercicio
```

Utilice el dataset **`estacion_meteorologica.csv`**:

a) Calcule y grafique las matrices de correlación y covariancia.

b) Identifique las variables más correlacionadas y grafíquelas unas vs. la otra en un gráfico de dispersión. Luego grafique cada una a lo largo del tiempo (para todas las fechas).

c) Identifique las variables menos correlacionadas y grafíquelas unas vs. la otra en un gráfico de dispersión. Luego grafique cada una a lo largo del tiempo (para todas las fechas).
