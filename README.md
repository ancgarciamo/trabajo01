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
Esta variable es el concepto de matricula el cual en promedio pagan los estudiantes.

### ADM_RATE_ALL
Tasa en la cual las personas que intentan inscribirse en la institucion son admitidas.

### NT4_PRIV y NT4_PUB
Estas variables excluyentes entre si , y estas indican en promedio cuanto deberia pagar un estudiante para poder garantizarse su asistencia normal a la institucion, ignorando conceptos como la matricula.


## Matriz de Coorelacion
Como podemos ver , usando las variables escogidas observamos que no tienen coeficientes de relacion muy altos entre ellos por ende pueden ser usados para la prediccion , en el caso de NPT4_PUB y NT4_PRIV ,son variables que son excluyentes entre si, por lo tanto , estas no tienen coorelacion entre ellas.

## Primer clustering (Instituciones Publicas)

Para este clustering usamos las variables previamente escogidas pero dejando de lado la variable NT4_PRIV

### Curva del codo
Usando la tecnica de la curva del codo podemos obtener un numero ideal de clusters para el modelo ,con esto vemos que el numero ideal de clusters es 4.

Imagen 1

### Dendrograma

Imagen 2

## Descripcion de los grupos

Grupo 1

Grupo 2

Grupo 3

Grupo 4



## Segundo clustering (Instituciones Privadas)

Para este clustering usamos las variables previamente escogidas pero dejando de lado la variable NT4_PRIV

### Curva del codo
Usando la tecnica de la curva del codo podemos obtener un numero ideal de clusters para el modelo ,con esto vemos que el numero ideal de clusters es 4.

Imagen 3

### Dendrograma

Imagen 4

## Descripcion de los grupos

Grupo 1

Grupo 2

Grupo 3

Grupo 4

## Uso por colombianos 

## Aplicacion

## Link del video 

## Conclusiones

## Referencias
