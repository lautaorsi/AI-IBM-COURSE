# Evaluación y Validación de Modelos


## Evaluación de Aprendizaje Supervisado
El proceso de evaluacion de un modelo involucra establecer su **precisión de predicción de resultados** y es fundamental para optimizar predicciones y entender la efectividad del mismo. 



## Métricas en clasificación

-   ###   Accuracy

Ratio de instancias predecidas correctamente sobre total de instancias.

$$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$

-   ### Matriz de confusión
Compara asignaciónes realizadas con su asignación real.

![Matriz de confusion generica](confusion_matrix.png)

-   ### Precision
Cuantas predicciones positivas eran realmente positivas

$$\text{Precision} = \frac{TP}{TP + FP}$$

-   ### Recall
Cuantas instancias positivas fueron correctamente predecidas

$$\text{Recall} = \frac{TP}{TP + FN}$$


-   ### F1
Combina [Precision](#precision) y [Recall](#recall) utilizando su media balanceada.

$$\text{F1} = \frac{2 * Precision * Recall}{Precision + Recall}$$
