# Random Forest

En resumen, se basa en la idea de crear múltiples arboles imparciales para luego obtener un resultado final.

En el caso de **clasificación** se utiliza un *esquema de votos* para definir la clase resultante, por otro lado en el caso de **regresión** se utiliza un *promedio de los resultados* para predecir el final.

En general la idea es partir el dataset de entrenamiento en n subconjuntos que generarán n arboles independientes, utilizados despues en paralelo para obtener la solución final.

## Ventajas
-   Puede manejar múltiples features sin problema
-   En datasets lo suficientemente grandes puede ser de los modelos mas certeros

## Desventaja
-   Es computacionalmente costoso
-   Tarda en predecir, al tener que pasar por múltiples arboles


