
## Regularización
Es una técnica para prevenir overfitting en modelos de regresión, se basa en la reducción de coeficientes grandes.

$$\text{Funcion Coste Regularizado} = \text{MSE} + \text{$\lambda$} * \text{Penalizacion}$$

> -  $\lambda$ es el hiperparametro de regularización <br>
> - _Penalizacion_ puede ser del tipo Ridge, Lasso, etc

### Penalizaciones
Dentro de los mas notables tenemos:
-   Ridge  
        $$\text{$\lambda$} ||\text{$\theta$}||_{2} = \text{$\lambda$} \sum^{n}_{i=1}{\text{$\theta$}^{2}_{i}} $$
-   Lasso
        $$\text{$\lambda$} ||\text{$\theta$}||_{1} = \text{$\lambda$} \sum^{n}_{i=1}{|\text{$\theta$}_{i}|} $$

En general, el metodo Lasso es el que mejor resultados genera, pero va a depender mayoritariamente del esparcimiento del Dataset Y SNR