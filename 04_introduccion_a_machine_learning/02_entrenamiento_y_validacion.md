# Marco conceptual

## Métodos de Estimación

### Métodos Paramétricos

Tiene un approach de dos pasos:

1. Asumir la forma de la función $$f$$, la cual carga con alguna cantidad de parámetros dados para la forma.
2. Estimada la forma, i.e., seleccionado un modelo, se realiza algún procedimiento que use los datos de entrenamiento para entrenar el modelo a partir de estimar los parámetros.\
   Una forma común de entrenamiento es (ordinary) least squares.

### Métodos No Paramétricos

No hacen assumptions específicas sobre $$f$$,. Se busca un funcional suave que aproxime a  $$f$$, y al no hacer assumptions, se tiene el potencial de hacer una mejor aproximación. No usa parámetros pero requiere de muchas observaciones.

## Prediction Accuracy - Model Interpretability (Trade-Off)

A más flexibilidad del modelo, menos interpretabilidad ( $$Y$$ en general más flexibilidad suele implicar más accuracy aunque ¡pero no siempre!).

No siempre y flexibilidad ⇒ más accuracy, pues modelos más flexibles son más propensos a overfitting.

Cuando inferencia es el objetivo, lo mejor es una técnica menos flexible. Para predicción, una más flexible.

## Tipos de Aprendizaje

### Supervisado

Son los modelos hablados hasta ahora. Dada una observación i y un vector de medidas $$x_i$$ , existe una respuesta $$y_i$$ asociada.

Lo que se busca es entrenar un modelo que relacione la respuesta con los predictores.

No Supervisado

### No Supervisado

Dada una observación $$i = 1,\dots, n$$ , se tiene un vector de medidas xᵢ pero no una respuesta $$y_i$$ .

El objetivo es entender relaciones entre las variables, buscando posiblemente agrupar observaciones.

### Semi Supervisado

Cuando de entre los $$n$$ observaciones un subconjunto tiene respuestas y el otro restante no.

## Clasificación vs Regresión

* **Regresión:** Problemas con respuestas cuantitativas, i.e., numéricas.
* **Clasificación:** Problemas con respuestas categóricas o cualitativas.

Existen métodos que funcionan para ambos.

