# Reducción de Dimensionalidad
Es la idea de poder visualizar con facilidad clusters de dimensiones altas, en general se utiliza para [Modelos de Aprendizaje no Supervisado](../Unsupervised-Learning/) y permite aumentar la eficiencia a la hora de formar dichos clusters.<br>

Dentro de los metodos de reduccion de dimensionalidad tenemos:
-   [PCA](./PCA/) <br>
    Utilizado particularmente en reducciones lineales de dimensiones, permite interpretaciones sencillas y reduce el ruido. 
-   [t-SNE](./t-SNE) <br>
    Utilizado en reducciones no lineales, es particularmente bueno para visualizar grandes dimensiones pero computacionalmente costoso.
-   [UMAP](./UMAP/) <br>
    Utilizado en cualquier contexto, es bueno reteniendo la estructura global y de alto rendimiento, sin embargo depende mucho de sus hiperparametros para un funcionamiento adecuado.