# Agrupamiento de instituciones de educacion superior

## Introduccion
Para este trabajo se creara una aplicacion que le permita mostrar a un estudiante una base de datos con la cual esta podra ayudarle a tomar decisiones , ademas de una recomendacion de una institucion dependiendo un gusto particular de un persona.

## Pre procesamiento de datos
Como queremos recomendar instituciones de educacion superior , tenemos que recomendar instituciones que se encuentre actualmente activas, por ello tomamos la variable CUROPPER, la cual nos indica si la institucion se encuentra activa.

## Seleccion de variables
Para el trabajo se seleccionaran que se consideran que pueden ser de interés para el usuario las cuales son las siguientes

- HIGHDEG
- DISTANCEONLY
- ADM_RATE_ALL
- NPT4_PUB
- NT4_PRIV
- TUITFTE

### HIGHDEG
Esta variable nos indica cual es el mayor rango de certificacion obtenido por una institucion en toda su historia
- 0, Non-degree-granting
- 1, Certificate degree
- 2, Associate degree
- 3, Bachelor's degree
- 4, Graduate degree

### TUITFTE
Esta variable es el concepto de matricula

## Matriz de coorelacion
Como podemos ver , usando las variables escogidas observamos que no tienen coeficientes de relacion muy altos entre ellos por ende pueden ser usados para la prediccion , en el caso de NPT4_PUB y NT4_PRIV ,son variables que son excluyentes entre si, por lo tanto , estas no tienen coorelacion entre ellas.
