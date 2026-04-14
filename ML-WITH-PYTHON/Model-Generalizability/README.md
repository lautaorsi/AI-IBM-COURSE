
## Regularización
Es una técnica para prevenir overfitting en modelos de regresión, se basa en la reducción de coeficientes grandes.

$$\text{Funcion Coste Regularizado} = \text{MSE} + \text{$\lambda$} * \text{Penalizacion}$$

> -  $\lambda$ es el hiperparametro de regularización <br>
> - _Penalizacion_ puede ser del tipo Ridge, Lasso, etc

### Penalizaciones
Dentro de los mas notables tenemos:
-   Ridge <br>  
Penaliza grandes coeficientes, ayuda a reducir el overfitting pero puede no funcionar bien en datos esparcidos.
        $$\text{$\lambda$} ||\text{$\theta$}||_{2} = \text{$\lambda$} \sum^{n}_{i=1}{\text{$\theta$}^{2}_{i}} $$
-   Lasso <br>
Penaliza el valor absoluto de los coeficientes, fomenta soluciones dispersas pero puede no funcionar bien con datasets que tengan multicolinealidads .
        $$\text{$\lambda$} ||\text{$\theta$}||_{1} = \text{$\lambda$} \sum^{n}_{i=1}{|\text{$\theta$}_{i}|} $$

En general, el metodo Lasso es el que mejor resultados genera, pero va a depender mayoritariamente del esparcimiento del Dataset Y SNR


## Pipelines
Es la idea de crear objetos que realizan multiples partes de un proceso de predicción, como el preprocesamiento y modelado. 

## Optimización de Hiperparametros
Los hiperparametros de un modelo afectan su efectividad, uno podría verse tentado a testear distintas combinaciones de hiperparametros y quedarse con el que mejor se desempeñe en los tests, sin embargo eso sería un overfitting del test split. <br> Veamos entonces que metodo utilizar para la optimización sin data leakage.

### N-Fold Cross-Validation
La técnica consiste en dividir el dataset en N folds que se usan como subsets de validación, luego de esto para cada combinación de hiperparametros y fold se entrena el modelo utilizando los N-1 otros folds. 


## Extra
Veremos en el laboratorio que scikit cuenta con un modulo GridSearchCV, basicamente lo que esto hace es crear una matriz combinatoria de los hiperparametros, con eso realiza Cross-Validation