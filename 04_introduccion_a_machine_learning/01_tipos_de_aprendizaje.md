# Estimación de f(x)

Dada una respuesta a la salida cuantitativa $$Y$$ y $$p$$ distintos predictores  $$x_1,x_2,\dots,x_p$$ ; asumiendo que existe una relación entre $$Y$$ y $$x = (x_1,x_2,\dots,x_p)$$. puede escribir de manera general como

$$
Y=f(x) + \epsilon
$$

Con  $$f$$ una función desconocida y  $$\epsilon$$ un error aleatorio independiente de $$X$$ tal que  $$E( \epsilon)=0$$&#x20;

El Aprendizaje Estadístico busca estimar dicha  $$f$$ para cumplir dos posibilidades

**Predicción:** En el caso en que las entradas $$X$$ son accesibles pero $$Y$$no, pues $$E( \epsilon)=0$$, podemos predecir  $$Y$$ usando

$$
\hat{f}(X)=\hat{Y}
$$

Donde  $$\hat{f}$$ es una estimación de  $$f$$ y  $$\hat{Y}$$ los resultados de predicción de  $$Y$$.

El Accuracy de  $$\hat{Y}$$ como predicción de  $$Y$$ depende de dos cantudades:

* Error reducible: Viene de estimación de  $$f$$ por $$\hat{f}$$. Con un mejor modelo para  $$\hat{f}$$ , este error puede disminuir.
* Error irreducible: Aún si  $$f=\hat{f}$$ ,  $$Y$$ es una función de  $$\epsilon$$ , que por definición no se puede predecir con  $$X$$.

Dadas  $$\hat{f}$$  y $$X$$ fijas, si analizamos el error cuadrático medio entre  $$Y$$ y  $$\hat{Y}$$ obtenemos

$$
\begin{aligned}
\mathbb{E}\big[(y - \hat{y})^2\big] 
&= \mathbb{E}\big[(f(X) + \varepsilon - \hat{f}(X))^2\big] 
= \mathbb{E}\big[(f(X) - \hat{f}(X) + \varepsilon)^2\big] \\
&= \mathbb{E}\big[(f(X) - \hat{f}(X))^2 + 2(f(x) - \hat{f}(X))\varepsilon + \varepsilon^2\big] \\
&= \mathbb{E}\big[(f(X) - \hat{f}(X))^2\big] 
+ 2\,\mathbb{E}\big[\varepsilon (f(X) - \hat{f}(X))\big] 
+ \mathbb{E}\big[\varepsilon^2\big].
\end{aligned}
$$

Como $$X$$  y $$\epsilon$$ son independientes y $$E[\epsilon]=0$$ , se cumple que

* &#x20;$$2 \cdot E[\epsilon \cdot (f(X)-\hat{f}(X)]=2 \cdot E[\epsilon] \cdot E[ f(X)-\hat{f}(X]=0$$&#x20;
* &#x20;$$Var(\epsilon)=E[ \epsilon^2] -E[\epsilon]^2 = E[\epsilon^2]$$

$$
\therefore E[(Y-\hat{Y})^2]=E[(f(X)-\hat{f}(X))^2]+Var(\epsilon)
$$

**Inferencia:** Aquí se busca estimar$$f$$ , pero es necesario conocer $$\hat{f}$$  para poder entender mejor preguntas sobre los datos como las siguientes:

* ¿Qué predictores están asociados con la respuesta?
* ¿Cuál es la relación entre la respuesta y cada predictor?
* ¿Podemos combinar las relaciones entre predictores y respuesta de manera lineal?
