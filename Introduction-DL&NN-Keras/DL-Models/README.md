# Modelos de Aprendizaje Profundo




## Redes Neuronales Convolucionales (CNN)

Son redes neuronles cuya funcionalidad se basa específicamente en el procesamiento de imagenes. 


### Capa de Entrada

Normalmente en las redes neuronales tenemos entradas vectorizadas de tamaño $(N \times 1)$, sin embargo en el contexto de las CNN vamos a procesar imagenes y por lo tanto tenemos entradas de tamaño $(N \times M \times 1)$ si la imagen es en escala de grises y $(N \times M \times 3)$ si es _rgb_ .

### Capa Convolucional

Es la capa en la cual definimos filtros sobre la imagen


### Capa de Agrupación 

En esta capa reducimos las dimensiones de la información pasada por la red, tenemos 2 metodos principales:

-   Max pooling 

    Tomamos el máximo del área analizada, esto es particularmente útil para la retención de objetos en la imágen incluso despues de reducir el espacio (el objeto reducido no mantiene semejanza con el original)

-   Average pooling
    
    Tomamos el promedio del área analizada


### Capa Totalmente Conectada

Esta capa se encarga de conectar todos los nodos de la última capa con todos los de la capa de salida, recibiendo el output de la capa anterior y enviando un vector de dimensión $N$, donde N es la cantidad de clases pertinentes al problema


## Redes Neuronales Recurrentes (RNN)

Este tipo de red neuronal se centra en el problema de tratar datapoints como instancias independientes entre sí, la idea está en que esta red toma -además del datapoint- el output de la red con el datapoint anterior.



## Transformadores

