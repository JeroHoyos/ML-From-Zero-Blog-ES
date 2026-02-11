# Estimación de f(x)

Dada una respuesta a la salida cuantitativa $$Y$$ y $$p$$ distintos predictores  $$x_1,x_2,\dots,x_p$$ ; asumiendo que existe una relación entre $$Y$$ y $$X = (x_1,x_2,\dots,x_p)$$. puede escribir de manera general como

$$
Y=f(x) + \epsilon
$$

Con  $$f$$ una función desconocida y  $$\epsilon$$ un error aleatorio independiente de $$X$$ tal que  $$E( \epsilon)=0$$&#x20;

El Aprendizaje Estadístico busca estimar dicha  $$f$$ para cumplir dos posibilidades

*

**Predicción:** En el caso en que las entradas $$X$$ son accesibles pero $$Y$$no, pues $$E( \epsilon)=0$$, podemos predecir  $$Y$$ usando

$$
\hat{f}(x)=\hat{Y}
$$

Donde  $$\hat{f}$$ es una estimación de  $$f$$ y  $$\hat{Y}$$ los resultados de predicción de  $$Y$$.
