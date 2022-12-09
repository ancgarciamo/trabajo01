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
|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PUB|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|482\.0|482\.0|482\.0|482\.0|482\.0|482\.0|482\.0|482\.0|482\.0|482\.0|
|mean|0\.002074688796680498|7448\.338174273859|0\.6719280082987551|13648\.724066390041|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|
|std|0\.0455487518674277|3281\.299536524236|0\.170883352707674|3818\.4300553949543|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|1217\.0|0\.18|2035\.0|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|
|25%|0\.0|5209\.25|0\.565675|11299\.25|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|
|50%|0\.0|6644\.5|0\.68145|13803\.5|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|
|75%|0\.0|9161\.75|0\.8052|16101\.25|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|
|max|1\.0|24891\.0|1\.0|27032\.0|0\.0|0\.0|0\.0|1\.0|0\.0|0\.0|

Grupo 2

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PUB|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|67\.0|67\.0|67\.0|67\.0|67\.0|67\.0|67\.0|67\.0|67\.0|67\.0|
|mean|0\.0|6200\.835820895522|0\.6811582089552238|13292\.89552238806|0\.0|0\.0|0\.9402985074626866|0\.0|0\.05970149253731343|1\.0|
|std|0\.0|9084\.257561426459|0\.24770117819984638|4923\.274117330213|0\.0|0\.0|0\.23872115183006284|0\.0|0\.23872115183006284|0\.0|
|min|0\.0|443\.0|0\.1364|328\.0|0\.0|0\.0|0\.0|0\.0|0\.0|1\.0|
|25%|0\.0|2875\.0|0\.5|10885\.5|0\.0|0\.0|1\.0|0\.0|0\.0|1\.0|
|50%|0\.0|4728\.0|0\.7143|12963\.0|0\.0|0\.0|1\.0|0\.0|0\.0|1\.0|
|75%|0\.0|7094\.0|0\.9128000000000001|16421\.0|0\.0|0\.0|1\.0|0\.0|0\.0|1\.0|
|max|0\.0|74228\.0|1\.0|23325\.0|0\.0|0\.0|1\.0|0\.0|1\.0|1\.0|

Grupo 3

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PUB|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|75\.0|75\.0|75\.0|75\.0|75\.0|75\.0|75\.0|75\.0|75\.0|75\.0|
|mean|0\.0|5336\.24|0\.6724853333333334|11836\.76|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|std|0\.0|3199\.4443049599317|0\.15067314516486963|4383\.148476066404|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|516\.0|0\.2547|2146\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|25%|0\.0|2981\.5|0\.56445|8843\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|50%|0\.0|5566\.0|0\.6488|11319\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|75%|0\.0|6941\.5|0\.8143|14971\.5|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|max|0\.0|15445\.0|1\.0|22976\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|

Grupo 4

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PUB|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|46\.0|46\.0|46\.0|46\.0|46\.0|46\.0|46\.0|46\.0|46\.0|46\.0|
|mean|0\.0|2614\.586956521739|0\.7291173913043478|7694\.739130434783|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|std|0\.0|2249\.356456866788|0\.16074435508228974|3624\.328440076298|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|151\.0|0\.3818|-445\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|25%|0\.0|1149\.5|0\.6321|5135\.75|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|50%|0\.0|2278\.0|0\.7295|7647\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|75%|0\.0|3102\.5|0\.85545|9858\.25|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|max|0\.0|12051\.0|1\.0|17639\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|


## Segundo clustering (Instituciones Privadas)

Para este clustering usamos las variables previamente escogidas pero dejando de lado la variable NT4_PRIV

### Curva del codo
Usando la tecnica de la curva del codo podemos obtener un numero ideal de clusters para el modelo ,con esto vemos que el numero ideal de clusters es 4.

Imagen 3

### Dendrograma

Imagen 4

## Descripcion de los grupos

Grupo 1

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PRIV|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|113\.0|113\.0|113\.0|113\.0|113\.0|113\.0|113\.0|113\.0|113\.0|113\.0|
|mean|0\.0|10124\.20353982301|0\.7887769911504424|18779\.159292035398|0\.0|0\.0|0\.7964601769911505|0\.0|0\.20353982300884957|0\.0|
|std|0\.0|6802\.198894946834|0\.2394310290671443|7728\.885353897107|0\.0|0\.0|0\.4044240180137636|0\.0|0\.4044240180137636|0\.0|
|min|0\.0|0\.0|0\.0|751\.0|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|25%|0\.0|5666\.0|0\.7059|14797\.0|0\.0|0\.0|1\.0|0\.0|0\.0|0\.0|
|50%|0\.0|8663\.0|0\.8388|19475\.0|0\.0|0\.0|1\.0|0\.0|0\.0|0\.0|
|75%|0\.0|13683\.0|1\.0|22972\.0|0\.0|0\.0|1\.0|0\.0|0\.0|0\.0|
|max|0\.0|36858\.0|1\.0|40545\.0|0\.0|0\.0|1\.0|0\.0|1\.0|0\.0|

Grupo 2

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PRIV|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|862\.0|862\.0|862\.0|862\.0|862\.0|862\.0|862\.0|862\.0|862\.0|862\.0|
|mean|0\.002320185614849188|15798\.883990719258|0\.640195939675174|22163\.228538283063|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|
|std|0\.04814032465654461|6330\.564798981115|0\.19366829868052285|6819\.411575391628|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|370\.0|0\.0484|1172\.0|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|
|25%|0\.0|11596\.25|0\.5261750000000001|17997\.75|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|
|50%|0\.0|14923\.0|0\.66545|21587\.5|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|
|75%|0\.0|18950\.75|0\.7664249999999999|26120\.0|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|
|max|1\.0|48657\.0|1\.0|43952\.0|0\.0|0\.0|0\.0|1\.0|0\.0|1\.0|

Grupo 3

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PRIV|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|425\.0|425\.0|425\.0|425\.0|425\.0|425\.0|425\.0|425\.0|425\.0|425\.0|
|mean|0\.002352941176470588|16158\.748235294117|0\.6994028235294117|20732\.922352941176|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|std|0\.048507125007266595|6878\.1251569503|0\.21319931500015937|6834\.936500311934|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|0\.0|0\.0|1539\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|25%|0\.0|10778\.0|0\.5816|17364\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|50%|0\.0|16157\.0|0\.7486|21733\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|75%|0\.0|21553\.0|0\.8388|24111\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|
|max|1\.0|44463\.0|1\.0|45774\.0|0\.0|1\.0|0\.0|0\.0|0\.0|2\.0|

Grupo 4

|index|DISTANCEONLY|TUITFTE|ADM\_RATE\_ALL|NPT4\_PRIV|HIGHDEG\_ Associate degree|HIGHDEG\_ Bachelor&\#39;s degree|HIGHDEG\_ Certificate degree|HIGHDEG\_ Graduate degree|HIGHDEG\_ Non-degree-granting|Labels\_3Clusters|
|---|---|---|---|---|---|---|---|---|---|---|
|count|177\.0|177\.0|177\.0|177\.0|177\.0|177\.0|177\.0|177\.0|177\.0|177\.0|
|mean|0\.005649717514124294|14831\.23163841808|0\.818280790960452|21149\.129943502823|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|std|0\.07516460280028289|7019\.160330636076|0\.18569710697263755|7353\.350057507531|0\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|min|0\.0|0\.0|0\.2|1627\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|25%|0\.0|10058\.0|0\.7484|17888\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|50%|0\.0|13507\.0|0\.8388|21299\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|75%|0\.0|19465\.0|1\.0|23509\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|
|max|1\.0|61621\.0|1\.0|72265\.0|1\.0|0\.0|0\.0|0\.0|0\.0|3\.0|

## Uso por colombianos 

## Aplicacion

## Link del video 

## Conclusiones

## Referencias
