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

### Desvanecimiento del Gradiente 

El problema del desvanecimiento del gradiente se da principalmente al utilizar la función de activación sigmoidea, todo recae en que los valores de la función estan acotados entre 0 y 1 causando que los ajustes de las capas iniciales sean prácticamente nulos. 

## Funciones de Activación

A raíz del problema del Desvanecimiento del Gradiente es que vamos a nombrar algunas de las funciones de activación más relevantes 

-   ReLU 

    De las funciones más utilizadas, no "prende" las señales de neuronas con valores negativos (Si su resultado es negativo lo deja en 0 y por lo tanto no aporta nada a la siguiente capa).

$$ReLU(z) = \text{max(0,z)}$$


-   Softmax

    Una función particularmente útil en problemas de clasificación utilizada idealmente en la capa de salida para definir la probabilidad de las categorías. Esta efectividad en problemas de decisión se debe a que es una función sigmoide ocn el mismo rango de valores entre 0 y 1, transformando cualquier valor numerico anterior a la capa de salida en un valor interpretable como probabilístico. 

    
    $$Softmax(z) = \frac{e^{Z_{j}}}{\sum_{k=1}^{m}e^{Z_{k}}}$$

-   Tangente Hiperbólica

    Similar a la funcion sigmoidea pero con una simetria dada por su rango entre -1 y 1, si bien es parcialmente mejor en temas de desvanecimiento del gradiente con respecto a la sigmoidea sigue siendo propensa a caer en la misma problemática.

    $$tanh(z) = \frac{e^{z}-e^{-z}}{e^{z}+e^{-z}}$$


