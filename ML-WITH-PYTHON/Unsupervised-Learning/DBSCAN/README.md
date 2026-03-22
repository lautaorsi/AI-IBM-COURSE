# DBSCAN

Se basa en clustering espacial basandose en la densidad de los datapoints, este valor de densidad es definido por el usuario y luego se crean núcleos espaciales que centran los clusters.

## Parametros
Toma un N y un Epsilon, esto es utilizado para la clasificación de los datapoints en las siguientes categorías:
-   Core: Tiene al menos N points dentro del vecindario
-   Border: Puntos no *Core* dentro del vecindario del *Core* 
-   Noise: Aislado de cualquier *Core* y su respectivo vecindario.

## Pseudo-algoritmo
1.  No iterativo
2.  Arma los clusters en una pasada sin actualizarlos una vez clasificados
3.  Cualquier punto sin asignar se toma como ruido
