# Resumen: Regresión Logística y Clasificación

## Regresión Logística

### ¿Para qué sirve?
Se utiliza para predecir la **probabilidad** de que una observación pertenezca a una de dos clases (clasificación binaria). A pesar de su nombre, no se usa para predecir valores numéricos abiertos (como el precio de una casa), sino para categorizar.

### Info útil:
Es fundamental marcar un **threshold** o límite de decisión para diferenciar positivos de negativos. Por ejemplo, si la probabilidad es > 0.5, se clasifica como 1 (positivo); si es menor, como 0 (negativo).

### Cómo entrenar:
La métrica para calcular la efectividad es una función de costo llamada **pérdida logística** (Log Loss). Buscamos minimizarla porque mide qué tan bien la probabilidad predecida $\hat{p}_i$ se ajusta a la clase real $y_i$. Para lograr esto, se utiliza el **Descenso de Gradiente**, que ajusta los parámetros del modelo hasta encontrar el mínimo de la función de costo.


### Ejemplos de uso:
- Estimar si un paciente tiene una enfermedad (Sí/No) en base a peso, altura y presión arterial.
- Predecir si un usuario va a comprar un producto (Compra/No compra) según su edad y salario.

### Diferencia con Árboles
- **Regresión Logística:** Es un modelo paramétrico que usa la función sigmoide para devolver una probabilidad continua entre 0 y 1 antes de clasificar.
- **Árbol de Clasificación:** Es un modelo no paramétrico que divide los datos en ramas según reglas lógicas (ej: "Si edad > 30..."). 
- **Nota importante:** No confundir con el **Árbol de Regresión**, que es el que se usa para predecir valores continuos (temperaturas, índices demográficos, etc.).

---

# Clasificación
**Es el proceso de utilizar modelos ya entrenados para asignar etiquetas o categorías a nuevos datos.**

## Algoritmos de clasificación
Entre los más conocidos están:
* Regresión Logística
* Árboles de Decisión
* Redes Neuronales
* K-nearest neighbors (KNN)

## Clasificación de múltiples clases
Cuando un algoritmo es binario por naturaleza (como la Logística), usamos estrategias para clasificar en más de dos categorías:

1. **Uno contra todos (One-vs-Rest):** Se entrena un clasificador binario por cada etiqueta. El dato pasa por todos y gana la etiqueta que devuelva la probabilidad más alta.
   - *Ejemplo:* ¿Es azul? (Prob: 0.1) -> ¿Es verde? (Prob: 0.7) -> ¿Es rojo? (Prob: 0.2). Resultado: Verde.

2. **Uno contra uno (One-vs-One):** Se entrenan clasificadores para cada par posible de clases (ej: Azul vs Rojo, Rojo vs Verde, Verde vs Azul). Cada uno "vota" por una clase y gana la que tenga más votos acumulados.