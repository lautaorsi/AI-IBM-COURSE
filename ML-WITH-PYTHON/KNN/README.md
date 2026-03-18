# KNN
Es un algoritmo de aprendizaje supervisado, usa proximidad entre puntos para predicciones  y es utilizado en regresión y clasificación.


### Funcionamiento

Para modelos de clasificación se toma como valor predecido la clase mas popular entre los valores cercanos.<br>
Para modelos de regresión se calcula la media de los valores cercanos.


### Optimización del k
1. Testear un rango de valores k
2. Elegir k = 1 y calcular accuracy
3. Repetir incrementando k
4. Elegir el de mayor accuracy

### Notas
Es importante evitar features irrelevantes, dado que agrega mucho ruido que requiere un K mas elevado, el cual consecuentemente incrementa el costo computacional y disminuye el accuracy