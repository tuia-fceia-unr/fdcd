# Unidad 5. Transformación de datos - Práctica

```{rubric} Datasets
:class: rubric-datasets
```

| Dataset | Ejercicio/s | Descripción |
| --- | --- | --- |
| [`exoplanets.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/exoplanets.csv) | 1 | Exoplanetas confirmados al 30/10/2026, extraídos de la tabla *Planetary Systems Composite Parameters* del Archivo de Exoplanetas de la NASA. Incluye, entre otras variables, el periodo orbital, el semieje mayor de la órbita, la masa del planeta, el año y el método de descubrimiento. |
| [`data_variables.xlsx`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/data_variables.xlsx) | 2 | 2500 observaciones de cinco variables cuantitativas (`X1` a `X5`). |
| [`202207_PAX15min-ABC.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/202207_PAX15min-ABC.csv) | 3 | Cantidad de pasajeros por molinete y por estación, en intervalos de 15 minutos, de las líneas A, B y C del subte de la Ciudad Autónoma de Buenos Aires durante julio de 2022 (portal de datos abiertos BA Data). |
| [`llegadas_turistas.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/llegadas_turistas.csv) | 4 | Serie de tiempo de llegadas totales de turistas a la Argentina en un período de 20 años. |
| [`var_salidas.csv`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/var_salidas.csv) | 4 | Serie de tiempo de las variaciones de las salidas de turistas desde la Argentina, para un período más corto. |
| [`comentarios.txt`](https://raw.githubusercontent.com/tuia-fceia-unr/fdcd/main/unidades/u5-transformacion-datos/datasets/comentarios.txt) | 5 | Comentarios publicados en redes sociales sobre el lanzamiento de un producto, uno por línea. |

```{rubric} Ejercicio 1
:class: rubric-ejercicio
```

Los **exoplanetas o planetas extrasolares** son planetas que orbitan alrededor de otras estrellas que se encuentran más allá de nuestro sistema solar. El dataset `exoplanets.csv` , extraído del [**Archivo de Exoplanetas de la NASA**](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=PSCompPars), registra los descubrimientos de exoplanetas que han sido reportados a la fecha en publicaciones científicas revisadas por pares y confirmados utilizando varios métodos de detección y/o técnicas analíticas.

1. El **periodo orbital** de un exoplaneta (`pl_orbper`) es el tiempo que tarda dicho planeta en dar una vuelta completa alrededor de la estrella que orbita (en días terrestres). 
    
    a) Realice una descripción general de dicha variable que incluya tipo de variable, valores mínimo y máximo que toma y presencia de datos faltantes. 
    
    b) Un astrónomo se propone estudiar la distribución del periodo orbital de los exoplanetas descubiertos hasta la fecha y decide, en primera instancia, representar todos los registros a través de un histograma. Utilizando los valores observados de la variable de interés y unas pocas líneas de código obtiene el siguiente gráfico:
    
    ![Histograma del periodo orbital de los exoplanetas](imagenes/histograma.png)

    - ¿Considera que el gráfico anterior es representativo de la distribución real de la variable bajo estudio? ¿Qué podría hacer para mejorarlo?

    - Teniendo en cuenta su respuesta a la pregunta del ítem anterior, realice un histograma para representar la distribución de la variable **introduciendo las modificaciones que considere adecuadas**. ¿Qué puede decir acerca de la distribución del periodo orbital de los exoplanetas descubiertos?

    - Represente el periodo orbital de nuestro planeta en el gráfico realizado en el ítem anterior (365.25 días) y calcule el porcentaje de exoplanetas que poseen años más extensos que el año terrestre, considerando solo los exoplanetas con periodo orbital registrado.

2. Construya un gráfico que permita visualizar la distribución del número de planetas extrasolares encontrados según año (`disc_year`) y método de descubrimiento (`discoverymethod`), **en el que la variable temporal se encuentre categorizada en lustros** (periodos de 5 años). Comente brevemente lo observado.

3. Tomando en cuenta **únicamente los exoplanetas descubiertos mediante las técnicas de velocidad radial (`Radial Velocity`), tránsito (`Transit`) y detección directa (`Imaging`)**, construya un gráfico que le permita visualizar, en forma conjunta, el periodo orbital y la masa (`pl_bmasse`, expresada en masas terrestres) de los planetas según el método a través del cual se detectaron. ¿Encuentra diferencias en las características de los exoplanetas descubiertos por las distintas técnicas?

4. Johannes Kepler fue un astrónomo y matemático alemán cuya principal contribución científica fue el descubrimiento las leyes que rigen el movimiento de los planetas. Según la Tercera Ley de Kepler del movimiento planetario, el cubo del semieje mayor de la órbita de un planeta ($a$, columna `pl_orbsmax`, en unidades astronómicas) es proporcional al cuadrado de su periodo orbital ($P$). El semieje mayor equivale a la mitad de la suma de las distancias máxima y mínima del planeta a su estrella, por lo que suele interpretarse como su distancia media:

    $$a^3 = kP^2$$
    
    La constante $k$ depende de la masa de la estrella. Si $a$ se expresa en unidades astronómicas, $P$ en años y la masa de la estrella $M_*$ en masas solares (columna `st_mass`), y se desprecia la masa del planeta frente a la de la estrella, la ley toma la forma $a^3 = M_* \, P^2$.

    a) Realizando las transformaciones que considere necesarias sobre las variables, verifique gráficamente el cumplimiento de la tercera ley de Kepler para los planetas extrasolares.

    b) Como los exoplanetas orbitan estrellas de masas distintas, $k$ no es la misma para todos. Repita el gráfico utilizando $a^3 / M_*$ en lugar de $a^3$. ¿Qué cambia respecto del gráfico anterior?
    

```{rubric} Ejercicio 2
:class: rubric-ejercicio
```

El dataset `data_variables.xlsx` contiene 2500 observaciones de 5 variables cuantitativas `X1` , `X2` , `X3` , `X4` y `X5`.

1. Represente las distribuciones de las variables del dataset en un único gráfico y describa brevemente las características gráficas de cada una de ellas.

2. En función a la respuesta al ítem anterior, ¿qué medida de posición le parece más adecuada para describir a cada uno de estos conjuntos de datos?

3. Realice el escalado de este grupo de variables a través de cada una de las técnicas presentadas en clase: **estandarización (*z-score*), escalado mín-máx, escalado por máximo absoluto y escalado robusto**. En cada caso, represente gráficamente las variables transformadas y comente brevemente lo observado.

```{rubric} Ejercicio 3
:class: rubric-ejercicio
```

El archivo `202207_PAX15min-ABC.csv` contiene la cantidad de pasajeros por molinete y por estación, en intervalos de 15 minutos, de las líneas A, B y C de la red de subtes de la Ciudad Autónoma de Buenos Aires (CABA) durante julio de 2022.

1. Realice el *binning* de la variable que corresponde a la hora inicial del intervalo de 15 minutos (columna `DESDE`) en los siguientes periodos a lo largo del día: de 5-9 hs., 9.15-12 hs., 12.15-15 hs., 15.15 - 18 hs., 18.15-21 hs., 21.15 -24 hs. Luego, represente gráficamente el total de pasajeros para cada día en cada rango horario y para cada una de las líneas de subte (un gráfico para cada línea de subte por separado). 

    ¿Hay algún rango horario en el que, en general, se observen más pasajeros que en los demás? ¿Presentan las tres líneas un comportamiento similar en cuanto a la cantidad total de pasajeros por rango horario?

2. Para cada línea, analice si los datos muestran alguna diferencia respecto de la cantidad total de pasajeros por rango horario entre días de semana (lunes a viernes) y fines de semana (sábado y domingo). Para ello, puede utilizar el atributo `.dt.dayofweek` de `pandas` (o el método `weekday()` de los objetos `date` de la librería `datetime`), que representa los días de la semana con números enteros, desde 0 para el lunes hasta 6 para el domingo.

3. Considere los siguientes períodos semanales, que incluyen solo los días hábiles:

    - Semana 1: 4 al 8 Julio 2022
    
    - Semana 2: 11 al 15 Julio 2022
    
    - Semana 3: 18 al 22 Julio 2022
    
    - Semana 4: 25 al 29 Julio 2022
    
    Teniendo en cuenta que las semanas 3 y 4 corresponden a las semanas de vacaciones de invierno en CABA, ¿se observan diferencias en la cantidad total de pasajeros por rango horario en cada línea durante esas semanas, respecto de las dos primeras?
    

```{rubric} Ejercicio 4
:class: rubric-ejercicio
```

En este ejercicio se trabaja con dos series de tiempo: las llegadas totales de turistas a la Argentina en un período de 20 años (`llegadas_turistas.csv`) y las variaciones de las salidas de turistas en un período más corto (`var_salidas.csv`).

1. Grafique ambas series de tiempo.

2. Aplique dos métodos de suavizado simple para cada serie y grafique cada serie con sus dos suavizados correspondientes. 

3. Según lo explicado en clase, ¿qué tipo de suavizado recomendaría para modelizar cada serie? ¿Por qué?

4. Según su respuesta anterior genere los suavizados que considere pertinentes.

5. Escriba un diagnóstico de la dinámica de turismo de nuestro país en los períodos estudiados, desarrollando las características que puede describir el fenómeno, apoyándose en los métodos utilizados en los puntos anteriores. 

```{rubric} Ejercicio 5
:class: rubric-ejercicio
```

Una empresa quiere evaluar la respuesta de sus clientes al lanzamiento de un nuevo producto. Para ello, recopiló comentarios publicados en distintas redes sociales y los guardó en el archivo `comentarios.txt`.

1. Utilizando la clase `SentimentIntensityAnalyzer` del módulo `nltk.sentiment`, obtenga el puntaje de sentimiento compuesto (`compound`) de cada comentario. Este puntaje toma valores entre -1 (sentimiento muy negativo) y 1 (sentimiento muy positivo).

2. Calcule el sentimiento promedio de todos los comentarios. ¿Los usuarios respondieron en forma positiva o negativa al lanzamiento del producto?

3. Clasifique cada comentario como positivo (`compound` ≥ 0,05), negativo (`compound` ≤ -0,05) o neutral (valores intermedios), y calcule el porcentaje de comentarios de cada clase. ¿Esta información confirma la conclusión del ítem anterior? ¿Por qué un promedio cercano a 0 no implica necesariamente que los comentarios sean neutrales?

4. Utilizando la función `word_tokenize()` de `nltk.tokenize`, separe los comentarios en palabras e identifique las más frecuentes. ¿Ayudan a explicar el resultado del análisis de sentimiento?
