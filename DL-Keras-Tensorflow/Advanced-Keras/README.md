# Keras Avanzado

Hasta ahora veniamos utilizando la API secuencial de Keras para modelos con capas simples y lineales. Ahora pasamos a la **API funcional**.

## API funcional

Esta API nos permite crear modelos con múltiples inputs/outputs, mayor flexibilidad y modularización/reutilización de los modelos.

## Capas personalizadas

Podemos además definir capas personalizadas, estas permiten encapsular operaciones y comportamientos específicos dentro de la capa en sí. Se definen mediante la declaración de una subclase de Layer con estos 3 métodos obligatorios:

-   `init` 
    -   Inicializa los atributos de la capa (privado)
-   `build`
    -   Crea los pesos de la capa, se llama únicamente en el primer llamado a la capa
-   `call`
    -   Define la lógica del forward pass


Veamos un ejemplo de la creación de una capa Densa

```python
class CustomDenseLayer(Layer):
    
    def __init__(self, units=32):
        super(CustomDenseLayer, self).__init__()
        self.units = units

    def build(self, input_shape):
        self.w = self.add_weight(shape=(input_shape[-1], self.units), initializer='random_normal', trainable=True)
        self.b = self.add_weight(shape=(self.uints,), initializer = 'zeros', trainable=True)
    
    #Call activates the output via ReLU
    def call(self, inputs):
        return tf.nn.relu(tf.matmul(inputs, self.w) + self.b)
```

> Esta capa densa tiene la particularidad de integrar la función de activación ReLU en su output, tal como podemos ver en la función `call`


## TensorFlow 2.x

