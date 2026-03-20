

## Clustering
Es una tecnica para agrupar datapoints basandose en similaridades. <br>
Se puede utilizar uno o mas features para el agrupamiento

-   Partition-based: *(K-Means)*
    -   Divide en grupos disjuntos
    -   Utilizando k-means (el método de clustering) identifica k clusters con la minima variación entre un central y maximizar diferencias con externos
    -   Escala bien con grandes datasets 

-   Density-based: *DBSCAN*
    -   Crea clusters de cualquier forma
    -   Útil en datasets con mucho ruido

-   Hierarchical:   *Aglomerativo / Divisivo* 
    -   Organiza la data en clusters anidados
    -   Clusters contienen sub-clusters
    -   Útil para encontrar relaciones entre clusters (en particular para datasets pequeños/medianos)

