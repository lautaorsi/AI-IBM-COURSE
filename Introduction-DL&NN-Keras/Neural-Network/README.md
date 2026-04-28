# Redes Neuronales (Artificales)

La idea detrás de las Redes Neuronales Artificiales está en agrupar en distintas capas un conjunto de Neuronas Artificiales (también llamadas Perceptrones), estas capas van a tener distintas funciones según el modelo pero en general tenemos 3 tipos: 

- Input Layer
- Hidden Layer(s)
- Output Layer. 

Estas capas van a comunicarse entre sí para procesar la información, tomando $N$ inputs (donde $N$ es la cantidad de nodos en la capa anterior) y calculando la suma ponderada con sus respectivos pesos (para cada $N_i$ existe un $W_i$) tal que el resultado de salida de la neurona es:

$$f(N*W + b)$$

Lo que hacemos además es pasar el resultado por una función activadora $f$ que básicamente aplica transformaciones no lineales a la suma ponderada.






## Entrenamiento
Para entrenar nuestra Red Neuronal tenemos un ciclo de entrenamiento que consiste en 5 partes:

1.  **<u>Forward Propagation**</u> <br>
    Pasamos al modelo un input del entrenamiento, se transmite la información desde la Input Layer hasta la Output Layer pasando por cualquier Hidden Layer que haya en el medio.

2.  **<u>Error Calculation</u>** <br>
    Comparamos el valor obtenido en nuestra capa de salida con el valor real para obtener el error cometido.

3.  **<u>Backpropagation**</u> <br>
    En este punto podemos calcular el impacto que tiene cada peso de arista y bias de nodo en el valor del error cometido obtenido en el paso 2.

4.  **<u>Gradient Descent</u>** <br>
    Por último, utilizamos el algoritmo de descenso del gradiente para ajustar los valores de cada peso y bias a fin de reducir el error, intentando minimizar la funcion de perdida.




 

