# Evaluación y Validación de Modelos


## Evaluación de Aprendizaje Supervisado
El proceso de evaluacion de un modelo involucra establecer su **precisión de predicción de resultados** y es fundamental para optimizar predicciones y entender la efectividad del mismo. 
<br>
Como bien sabemos, dentro del aprendizaje supervisado tenemos 2 categorías diferentes a la hora de definir el uso del mismo, *Regresión* y *Clasificación*. Claramente nuestras métricas van a ser diferentes para los casos de regresión vs clasificación, veamos los casos particulares: 

### Métricas en clasificación

Estudiamos la correctitud de las clasificaciones predecidas respecto a su clasificación real.

-   ####   Accuracy

Ratio de instancias predecidas correctamente sobre total de instancias.

$$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$

-   #### Matriz de confusión
Compara asignaciónes realizadas con su asignación real.

![Matriz de confusion generica](confusion_matrix.png)

-   #### Precision
Cuantas predicciones positivas eran realmente positivas

$$\text{Precision} = \frac{TP}{TP + FP}$$

-   #### Recall
Cuantas instancias positivas fueron correctamente predecidas

$$\text{Recall} = \frac{TP}{TP + FN}$$


-   #### F1
Combina [Precision](#precision) y [Recall](#recall) utilizando su media balanceada.

$$\text{F1} = \frac{2 * Precision * Recall}{Precision + Recall}$$


### Métricas en regresión

Estudiamos la capacidad del modelo de predecir valores continuos con exactitud

-   #### MAE
Mide el promedio absoluto de la diferencia entre el valor actual y el predecido, tiene la ventaja de dar resultados en las unidades de la variable objetivo.

$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$$

-   #### MSE
Calcula el promedio de la diferencia de cuadrados entre valores reales y predecidos. Al ser cuadrado hay una mayor penalización por error.

$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)²$$

-   #### RMSE
Similar a [MSE](#mse), mantiene las penalizaciones fuertes pero convierte el resultado a la unidad original de la variable objetivo.

$$\text{MAE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)²}$$

-   #### R²
Calcula el porcentaje de la variabilidad de la variable objetivo que es explicada por los features.
$$R^2 = 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y}_i)^2}$$


## Evaluación de Aprendizaje No Supervisado
En el caso del aprendizaje no supervisado, la gran mayoría de veces no tenemos un _ground truth_ para medir la eficacia de nuestros clusters y por lo tanto nuestras métricas son relativamente subjetivas. En todo caso, algunas de las métricas sin _ground truth_ son llamas Internas, mientras que utilizar datasets ya categorizados para las métricas se llaman Externas. Algunas de ellas son:

### Métricas Internas en Clustering

-   #### Silhouette score
Compara la coherencia interna de cada cluster y la separación con otros clusters. Tiene un rango de valores entre -1 y 1 y valores altos indican clusters bien definidos.


-   #### Davies-Bouldin Index
Mide el ratio de densidad del cluster y la lejanía con el más cercano. En este caso, valores bajos indican clusters mejor definidos

-   #### Inertia
Calcula la sumatoria de variación interna del cluster. Valores bajos indican clusters compactos.

### Métricas Externas en Clustering
Utiliza datos categorizados para evaluar la calidad de cada cluster, comparandolos con las categorias asignadas como _ground truth_

-   ### Indice Rand Ajustado
Mide la similaridad entre la realidad y los resultados, toma valores entre -1 y 1, tomando valores proximos a 1 como bien categorizados

-   ### Informacion Mutua Normalizada
Asigna un valor numerico a la informacion compartida entre clusters, su escala va de 0 a 1 donde 1 marca información idéntica y 0 marca cero informacion compartida.


-   ### Indice Fowlkes-Mallows
Realiza calculos geometricos en base a la media de precisión y recall para indicar la performance del cluster. Mayor valor indica mejor clustering.


## Evaluación de Modelos de Reducción de Dimensionalidad
Por último, en el contexto de modelos de reducción de dimensionalidad la métrica más importante es cuanta información se retuvo luego de haberse aplicado la reducción.