# Aprendizaje Profundo

Cuando hablamos de aprendizaje profundo hablamos del proceso de optimización de las predicciones de [Redes Neuronales](../Neural-Network/README.md) iterando sobre una serie de pasos detallados a continuación:

1.  **<u>Forward Propagation**</u> <br>
    Pasamos al modelo un input del entrenamiento, se transmite la información desde la Input Layer hasta la Output Layer pasando por cualquier Hidden Layer que haya en el medio.

2.  **<u>Error Calculation</u>** <br>
    Comparamos el valor obtenido en nuestra capa de salida con el valor real para obtener el error cometido.

3.  **<u>Backpropagation**</u> <br>
    En este punto podemos calcular el impacto que tiene cada peso de arista y bias de nodo en el valor del error cometido obtenido en el paso 2.

4.  **<u>Gradient Descent</u>** <br>
    Por último, utilizamos el algoritmo de descenso del gradiente para ajustar los valores de cada peso y bias a fin de reducir el error, intentando minimizar la funcion de perdida.


## Descenso del Gradiente

El descenso del gradiente es un algoritmo basado en buscar el mínimo valor posible en una función dada, generalmente se trata de encontrar un mínimo local aceptable para el costo que tiene obtener uno más óptimo (obtener un mínimo total implicaría una cantidad de cómputo imposible). <br> El algoritmo trabaja calculando la pendiente y obteniendo la dirección que disminuye el valor de la función (es por esto que dependiendo del punto de "partida" vamos a obtener distintos mínimos locales).
