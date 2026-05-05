# Funciones de Activación

Las funciones de activación existen para permitir que las redes neuronales aprendar relaciones no lineales entre valores. 

-   Sigmoide
    La función mas elemental, produce un valor de salida entre 0 y 1. Esta función por ejemplo se aplica en las regresiones lineales para obtener modelos de regresión logística. 

$$ \sigma(z) = \frac{1}{1 + e^{-z}}$$



-   ReLU 

    De las funciones más utilizadas, no "prende" las señales de neuronas con valores negativos (Si su resultado es negativo lo deja en 0 y por lo tanto no aporta nada a la siguiente capa).

$$ReLU(z) = \text{max(0,z)}$$


-   Softmax

    Una función particularmente útil en problemas de clasificación utilizada idealmente en la capa de salida para definir la probabilidad de las categorías. Esta efectividad en problemas de decisión se debe a que es una función sigmoide ocn el mismo rango de valores entre 0 y 1, transformando cualquier valor numerico anterior a la capa de salida en un valor interpretable como probabilístico. 

    
    $$Softmax(z) = \frac{e^{Z_{j}}}{\sum_{k=1}^{m}e^{Z_{k}}}$$

-   Tangente Hiperbólica

    Similar a la funcion sigmoidea pero con una simetria dada por su rango entre -1 y 1, si bien es parcialmente mejor en temas de desvanecimiento del gradiente con respecto a la sigmoidea sigue siendo propensa a caer en la misma problemática.

    $$tanh(z) = \frac{e^{z}-e^{-z}}{e^{z}+e^{-z}}$$




### Desvanecimiento del Gradiente 

El problema del desvanecimiento del gradiente se da principalmente al utilizar la función de activación sigmoidea, todo recae en que los valores de la función estan acotados entre 0 y 1, causando que los ajustes de las capas iniciales sean prácticamente nulos. 

