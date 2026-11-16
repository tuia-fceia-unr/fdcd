# Unidad 6. Ajustes y modelos - Práctica

| Dataset | Ejercicio/s | Descripción |
| --- | --- | --- |
| [`student_data.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u6-ajustes-y-modelos/datasets/student_data.csv) | 1 | Promedio de horas semanales de estudio y calificación final obtenida en un examen por un grupo de estudiantes. |
| [`advertising.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u6-ajustes-y-modelos/datasets/advertising.csv) | 4 | Ventas de un producto en 200 mercados y presupuesto publicitario destinado a televisión, radio y periódicos. |
| [`auto.xlsx`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u6-ajustes-y-modelos/datasets/auto.xlsx) | 5 | Consumo, potencia, peso y origen de 392 automóviles de distintas marcas y modelos. |
| [`nadadores.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u6-ajustes-y-modelos/datasets/nadadores.csv) | 6 | Variables antropométricas, tipo de entrenamiento y tiempo en los 100 metros libres de 50 nadadores de competición. |
| [`USA_Housing.xlsx`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u6-ajustes-y-modelos/datasets/USA_Housing.xlsx) | 7 | Características de 5000 viviendas de Estados Unidos y de las ciudades en las que se ubican, junto con su precio de venta. |

```{rubric} Ejercicio 1
:class: rubric-ejercicio
```

El dataset **`student_data.csv`** contiene el promedio de horas semanales que un grupo de estudiantes de una institución educativa dedicó a preparar un examen y la calificación final que obtuvo cada uno al rendirlo.

1. Construya un gráfico que permita visualizar la relación entre las calificaciones finales y las horas de estudio. ¿Cómo describiría esa relación a partir de lo observado?

2. ¿Qué medida utilizaría para cuantificar el grado de asociación lineal entre ambas variables? Calcúlela e interprete el valor obtenido.

3. Ajuste un modelo de regresión lineal para explicar la calificación final de los estudiantes de la institución a partir de las horas semanales de estudio y represéntelo sobre el gráfico del ítem 1.

4. Escriba la ecuación del modelo ajustado e interprete cada uno de sus coeficientes.

```{rubric} Ejercicio 2
:class: rubric-ejercicio
```

Se ajustó, por mínimos cuadrados, un modelo de regresión lineal múltiple para el precio de una propiedad, expresado en pesos, a partir de los siguientes predictores:

- $x_1$: superficie, en metros cuadrados.
- $x_2$: cantidad de habitaciones.
- $x_3$: antigüedad, en años.
- $x_4$: ubicación, codificada como 0 para el ámbito urbano y 1 para el suburbano.

Los coeficientes estimados fueron $\hat{\beta}_0 = 10000$, $\hat{\beta}_1 = 5000$, $\hat{\beta}_2 = 2000$, $\hat{\beta}_3 = -1500$ y $\hat{\beta}_4 = -15000$.

1. Escriba la ecuación del modelo ajustado.

2. A partir del modelo ajustado, ¿cuál de las siguientes afirmaciones es correcta? Justifique su elección y explique por qué las demás no lo son.

    a) Para un mismo número de habitaciones, antigüedad y superficie, las propiedades suburbanas son más caras, en promedio, que las urbanas.

    b) Para viviendas urbanas de igual superficie y cantidad de habitaciones, el precio predicho por el modelo aumenta, en promedio, \$10000 por cada año de antigüedad.

    c) El número de habitaciones tiene más peso sobre el precio en las viviendas urbanas que en las suburbanas.

    d) El modelo predice que una propiedad urbana cuesta \$15000 más que una propiedad suburbana de igual superficie, antigüedad y cantidad de habitaciones.

```{rubric} Ejercicio 3
:class: rubric-ejercicio
```

El dataset `penguins` reúne medidas corporales de pingüinos de tres especies (`species`) que anidan en el Archipiélago Palmer, en la Antártida: la longitud del pico (`bill_length_mm`), la profundidad del pico (`bill_depth_mm`), la longitud de la aleta (`flipper_length_mm`), la masa corporal (`body_mass_g`) y el sexo (`sex`). 

1. Importe el dataset al entorno de trabajo utilizando la función `load_dataset()` de la librería Seaborn. A continuación, descarte los registros con datos faltantes en las variables involucradas.

2. Construya un gráfico que permita visualizar la relación entre la longitud de la aleta y la longitud del pico, según la especie. ¿Qué observa?

3. Ajuste un modelo de regresión lineal para explicar la longitud promedio del pico a partir de la longitud de la aleta (**modelo 1**).

4. Teniendo en cuenta lo observado en el ítem 1, modifique el modelo inicial para mejorar su capacidad predictiva y ajuste el nuevo modelo (**modelo 2**).

5. ¿Cuál de los dos modelos proporciona un mejor ajuste? ¿Qué medida utilizó para compararlos?

6. Utilice el modelo seleccionado para predecir la longitud del pico de un pingüino macho de la especie Chinstrap con 191 mm de longitud de aleta, 17.6 mm de profundidad de pico y 3125 g de masa corporal.

```{rubric} Ejercicio 4
:class: rubric-ejercicio
```

Un cliente lo contrata como científico de datos para estudiar la asociación entre la inversión publicitaria de su empresa y las ventas de un producto. El dataset **`advertising.csv`** contiene las ventas (`Sales`) de ese producto en 200 mercados y los presupuestos publicitarios destinados a televisión (`TV`), radio (`Radio`) y periódicos (`Newspaper`).

1. ¿La inversión en cuál de los tres medios se asocia más fuertemente con las ventas? Fundamente su respuesta.

2. Ajuste un modelo de regresión lineal múltiple para modelar las ventas (*Sales*) en función de los tres presupuestos publicitarios (*TV*, *Radio* y *Newspaper*). En base a las pruebas de hipótesis sobre los parámetros del modelo, evalúe si corresponde ajustar un modelo con menos predictores y justifique cada decisión que tome.

3. Escriba la ecuación del modelo ajustado final e interprete el coeficiente correspondiente a `TV`.

4. Utilice el modelo para estimar las ventas promedio de un mercado con una inversión de 150 mil USD en televisión, 30 mil USD en radio y 60 mil USD en periódicos.

5. Represente gráficamente la distribución de los residuos del modelo y describa sus características. ¿Puede suponerse que se cumple el supuesto de normalidad?

```{rubric} Ejercicio 5
:class: rubric-ejercicio
```

El dataset **`auto.xlsx`** contiene información sobre 392 automóviles de distintas marcas y modelos. Entre sus columnas se encuentran el consumo en millas por galón (`mpg`, 1 galón equivale a aproximadamente 3.785 litros), la potencia en caballos de fuerza (`horsepower`), el peso en libras (`weight`), el origen (`origin`) y la marca y el modelo (`name`).

1. ¿Qué porcentaje de los automóviles del dataset pertenece a la marca *Ford*?

2. Construya un gráfico que permita visualizar la distribución de los automóviles según su origen. Para ello, tenga en cuenta que la columna `origin` está codificada de la siguiente manera: 1 = americano, 2 = europeo y 3 = japonés.

3. Ajuste un modelo de regresión lineal simple con el consumo como variable respuesta y la potencia como único predictor. A partir de los resultados, responda:

    a) ¿La relación entre ambas variables es positiva o negativa?

    b) ¿Cómo interpreta el coeficiente correspondiente a `horsepower`?

    c) ¿Qué porcentaje de la variabilidad del consumo es explicada el modelo?

4. Construya un gráfico que muestre la relación entre `mpg` y `horsepower` y represente sobre él la función de regresión estimada. ¿Encuentra alguna limitación en el modelo propuesto? Justifique.

5. Si su respuesta al ítem anterior fue afirmativa, proponga y ajuste una modificación del modelo que resuelva las limitaciones encontradas.

```{rubric} Ejercicio 6
:class: rubric-ejercicio
```

En un grupo de nadadores de competición se desea estudiar si algunas variables antropométricas (la estatura, el peso y el alcance de brazos) y el tipo de entrenamiento se relacionan con el tiempo en los 100 metros libres. El dataset **`nadadores.csv`** contiene los datos de 50 nadadores que participaron de un torneo inter-clubes:

- `tiempo`: tiempo en los 100 metros libres, en segundos.
- `estatura`: estatura, en centímetros.
- `peso`: peso, en kilogramos.
- `alcance_brazo`: alcance de brazos, en centímetros.
- `entrena_fuerza`: 1 si el nadador realiza entrenamiento de fuerza y 0 si no.
- `entrena_pasadas`: 1 si el nadador realiza entrenamiento de velocidad explosiva y 0 si no.

1. Construya gráficos separados que muestren la relación entre el tiempo en los 100 metros libres y cada una de las tres variables antropométricas (estatura, peso y alcance de brazos). ¿Cuál o cuáles de ellas parecen estar asociadas con el tiempo?

2. Ajuste un modelo de regresión lineal múltiple para el tiempo en los 100 mettos libres que incluya los cinco predictores. ¿Cuáles resultan significativos al 5 %?

3. En base a su respuesta del ítem anterior, evalúe la posibilidad de ajustar un modelo alternativo con un subconjunto de los predictores. Justifique su decisión y escriba la ecuación del modelo ajustado.

4. Utilice el modelo final para predecir el tiempo de un nadador de 188 cm de estatura que no realiza ninguno de los dos tipos de entrenamiento.

```{rubric} Ejercicio 7
:class: rubric-ejercicio
```

El dataset **`USA_Housing.xlsx`** contiene información sobre 5000 viviendas de Estados Unidos. Las variables que describen a cada vivienda son:

- `avg_area_income`: ingreso promedio de los residentes de la ciudad en la que se ubica la vivienda.
- `avg_area_house_age`: antigüedad promedio de las casas de esa ciudad.
- `avg_area_number_of_rooms`: número promedio de ambientes de las casas de esa ciudad.
- `avg_area_number_of_bedrooms`: número promedio de dormitorios de las casas de esa ciudad.
- `area_population`: población de la ciudad.
- `price`: precio de venta de la vivienda.
- `address`: domicilio de la vivienda.

**Parte I. Análisis exploratorio**

1. Importe el dataset y realice las tareas de limpieza y adecuación que considere necesarias para su análisis.

2. Construya un gráfico que permita visualizar la distribución del precio de venta. A partir del gráfico, ¿cómo describiría la distribución en cuanto a su simetría?

3. Construya un gráfico que permita evaluar el grado de asociación lineal entre las variables cuantitativas del dataset. Identifique el par de variables más fuertemente correlacionadas e interprete la medida de asociación correspondiente.

4. Elija uno de los pares de variables identificados en el ítem anterior y construya un gráfico que permita visualizar la relación entre ellas.

**Parte II. Ajuste del modelo**

El objetivo de esta parte es analizar si es factible ajustar un modelo de regresión lineal que permita predecir el precio de venta de una vivienda a partir de la población y el ingreso promedio de la ciudad en la que se ubica, así como de las características generales de las viviendas de esa ciudad (antigüedad promedio, número promedio de ambientes y de dormitorios).

1. Ajuste el modelo completo, que incluya todas las variables explicativas de interés. ¿Cuáles de ellas contribuyen significativamente a explicar el precio de venta? Justifique.

2. A partir de su respuesta anterior, ajuste un nuevo modelo y, con base en él:

    a) Escriba la ecuación del modelo ajustado e interprete cada uno de sus coeficientes.

    b) ¿Qué medida utilizaría para comparar el modelo completo con el nuevo modelo en cuanto a su bondad de ajuste? Interprete su valor para el modelo final.

    c) Construya un gráfico de valores predichos vs. valores reales y comente lo observado.