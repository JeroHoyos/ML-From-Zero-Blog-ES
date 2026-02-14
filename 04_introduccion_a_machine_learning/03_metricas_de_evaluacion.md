# Métricas de Error

### Regresión

Sea $$\hat{f}$$ obtenida de un modelo entrenado con los datos  $$\{(x_1,y_1), \ldots, (x_n,y_n)\}$$ donde $$y_i$$ es numérica.

#### Mean Squared Error (MSE)



$$
\frac{1}{n} \sum^{n}_{i=1} (y_i-\hat{f}(x_i))^2 = E[(y_i-\hat{y})^2]
$$

Buscamos minizar el MSE, donde su mínimo está dado por

$$
E[(y_i-\hat{y})^2] = Var(\epsilon)
$$

### Clasificación

Sea $$\hat{f}$$ obtenida de un modelo entrenado con los datos  $$\{(x_1,y_1), \ldots, (x_n,y_n)\}$$ donde $$y_i$$ es categórica.

#### Error Rate

$$
\frac{1}{n} \sum^{n}_{i=1} I(y_i \neq \hat{y_i}), \quad \text{donde} \quad I(y_i \neq \hat{y_i}) \begin{cases} 1, \quad \text{si} \quad y_i\neq \hat{y}_i \\0, \quad \text{si} \quad y_i= \hat{y}_i \end{cases}
$$

Buscamos minizar el Error Rate, donde su mínimo está dado por

$$
\forall i \quad I(y_i \neq \hat{y}_i) =0
$$
