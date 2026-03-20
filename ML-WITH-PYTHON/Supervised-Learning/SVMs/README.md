# Support Vector Machines

Es una tecnica de aprendizaje supervisado para construir modelos de clasificacion y regresion, utilizando hiperplanos de segregación y valores de cada feature como puntos de una coordenada.

En su núcleo, los SVM son únicamente para problemas de clasificación binaria, pero estos pueden ser adaptados para la regresión.  

### Kerneling
Es la idea de mapear data en un espacio de mayor dimension que el original utilizando un kernel (funciones que toman features), algunos de estos: <br>
Lineales, polinomiales, RBF y sigmoides 

## Ventajas 
-   Efectivo en espacios de grandes dimensiones
-   Robusto contra overfitting
-   Altamente eficaz en datos linealmente separables
-   Funciona con datos difusos en su clasificación

## Desventajas
-   Lento para entrenar con datasets de gran tamaño
-   Sensible al ruido y casos de superposición
-   Sensible al kernel y parametros de regularización

## Usos 
-   Clasificación de imagenes
-   Detección de spam/anomalías