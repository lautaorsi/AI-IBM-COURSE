# Modelos de Aprendizaje Profundo




## Redes Neuronales Convolucionales (CNN)

Son redes neuronles cuya funcionalidad se basa específicamente en el procesamiento de imagenes, esto permite otro tipo de inputs distintos a los de las redes  neuronales simples, en las que tenemos entradas vectorizadas de tamaño $(N \times 1)$. 


### Capa de Entrada
En el contexto de las CNN vamos a procesar imagenes y por lo tanto tenemos entradas de tamaño $(N \times M \times 1)$ si la imagen es en escala de grises y $(N \times M \times 3)$ si es _rgb_ .

### Capa Convolucional

Es la capa en la cual definimos filtros sobre la imagen. Además esta capa contiene funciones ReLU para filtrar el resultado, anulando valores negativos.


### Capa de Agrupación 

En esta capa reducimos las dimensiones de la información pasada por la red, tenemos 2 metodos principales:

-   Max pooling 

    Tomamos el máximo del área analizada, esto es particularmente útil para la retención de objetos en la imágen incluso despues de reducir el espacio (el objeto reducido no mantiene semejanza con el original)

-   Average pooling
    
    Tomamos el promedio del área analizada


### Capa Totalmente Conectada

Esta capa "aplasta" la salida de la última capa convolucional y se conecta con todos los nodos de la capa siguiente.


## Redes Neuronales Recurrentes (RNN)

Este tipo de red neuronal se centra en el problema de tratar datapoints como instancias independientes entre sí, la idea está en que esta red toma -además del datapoint- el output de la red con el datapoint anterior.



## Transformadores

Los transformadores se especializan en relacionar distitnas partes de una secuencia de entrada y mecanismos de atención. El mecanismo de atención esta compuesto por tres partes:

1.  Generación de Vectores Query, Key y Value
    -   ***Query*** Embedding vectorial de la informacion que busca el token
    -   ***Key***   Representación de la información que contiene cada token
    -   ***Value*** Información contextual del token
    

2.  Puntaje de Atención (Attention scores)
    Calcula la atencion que un token le presta a otro.  Este puntaje se obtiene de la siguiente manera:
    1. El producto del vector Query de cada token con todos los vectores key de los otros tokens
    2. Se escala el vector resultante diviendolo por la raíz de la dimension de los vectores
    3.  Aplicamos la función softmax a cada valor del vector para obtener una sumatoria de 1 (algo así como obtener el _porcentaje de atención_)

3.  Suma ponderada
    El último paso es obtener la informacion contextual del token, esto se logra multiplicando el vector de porcentaje de atención por la información contextual de todos los otros tokens. 
    
> Todas estas operaciones se pueden aplicar de forma paralela, resultando en tiempos de entrenamiento mucho mas rápidos que otros modelos.

