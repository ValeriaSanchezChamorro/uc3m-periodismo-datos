# ¿Qué se festeja más en Twitter?

En el presente trabajo se pretende exponer los resultados obtenidos tras el análisis de los datos del **proyecto _TRESCA_**. Apartir de las informaciones vertidas en el documento CSV _feliz.csv_ se han realizado dos gráficos relacionados con la felicitación de determinadas celebraciones en Twitter. Para obtener los resultados finales se ha limpiado, operado y ordenado el contenido del CSV mediante _OpenRefine_. Finalmente se han trasladado los datos a _Datawrapper_ para conseguir las representaciones gráficas.  

## Trabajando con los datos

Las Redes Sociales son estructuras de Internet en las que los individuos se relacionan de forma rápida. Además, operan en distintos niveles (uno puede utilizar las redes para relacionarse, pero también para su ámbito profesional). Sin embargo, siempre permiten ese intercambio de informaciones ilimitado. Estas redes se utilizan principalmente para comunicarse, pero también sirven para informarse, entretenerse, compartir contenidos y opiniones o comprar productos, entre muchos otros usos. Desde las Redes Sociales es incluso posible convocar manifestaciones masivas. En definitiva, sirven para casi todo lo que se puede imaginar. 

La primera dificultad que se ha encontrado en el documento reside en que los datos con los que se ha trabajado no representan la realidad en su totalidad. Todos aquellos días en los que los _#Hashtags_ no han superado los 10.000 tweets no son contabilizados en el CSV. Por lo tanto, las informaciones con las que se cuenta son una estimación. En _OpenRefine_ se han seleccionadolos datos más interesantes para su representación. Así, se han seleccionado aquellos relacionados con las festividades y se ha desechado el resto. 

Para la creación de los gráficos se ha escogido un período de tiempo delimitado. El año 2020 resulta más interesante en cuantoa cantidad de Tweets a pesar del tramo sin informaciones de los meses de verano. Esto se debe a que diciembre es especialmenteactivo en Twitter. Para trabajar con estos datos se ha creado una **faceta temporal** y se ha seleccionado este intervalo de tiempo (marzo 2020 – diciembre 2020). De este modo también se evita contar con los datos de 2021 relativos a las mismas festividades.  

![cluster.png](/img/cluster.png)

Después se ha procedido a eliminar las celdas vacías que no contenían el total de _#Hashtags_. Para ello se ha creado una **nueva faceta personalizada para celdas nulas** que separa filas en blanco y filas con datos. Después se han eliminado aquellas celdas vacías.  

Una vez eliminadas se ha utilizado la función **Cluster** para agrupar aquellos _#Hashtags_ que tratan la misma temática y quevarían solamente en algunos caracteres (por ejemplo, _#Feliz Dia de Navidad_ y _#FelizNavidad_). En la columna dedicada a los nombres de los _#Hashtags_ se ha usado la herramienta de **Editar texto**. Con ella se han cambiado varios caracteres de algunos tweets. Por ejemplo, se ha editado el nombre de la etiqueta _Feliz Año_ para que el _#Hashtag_ no tenga espaciado (#FelizAño). Este cambio se ha aplicado a toda la columna con la que se ha trabajado. 

![editar.png](/img/editar.png)

Dado que lo más relevante para el trabajo era exponer la cantidad de tweets sobre una fiesta en un año concreto, la columna _Fecha_ no resultaba relevante. Lo que se pretendía era realizar un _sumatorio del número de veces que se ha twitteado sobre unafestividad en el año 2020_. Para ello, en la columna en la que se encuentran los _#Hashtags_ se aplicó un **blankdown** que agrupa todos los nombres que se repiten de los seleccionados, dejando los ocho valores con los que se quería trabajar:

-       FelizNavidad (33.145.172)
-       FelizAño (6.345.842)
-       FelizDiadeLaMadre (683.633)
-       FelizDiaDelPadre (526.645)
-       FelizAlzamiento (480.126)
-       Feliz Halloween (315.544)
-       FelizDiaDelTrabajador (180.599)
-       Feliz Pascua (124.774)

![blank.png](/img.blank.png)

Por último, se ha utilizado la fórmula _row.record.cells ['Numero'].value.sum() para sumar el número total de _#Hashtags_ publicados sobre una misma fiesta. Para conseguir este resultado ha sido necesario crear una nueva columna sobre la dedicada al número de _tweets_ por _#Hashtag_, utilizando dicha fórmula. Así, se han contabilizado los resultados totales de las ocho fiestas más felicitadas en Twitter.

![suma.png](/img.suma.png)

## Representación gráfica y justificación 

Para la creación de los gráficos se ha utilizado tanto la academia de Datawrapper como el catálogo de la visualización de datos. 

![festividad1.png](/img/festividad1.png)

1. El siguiente gráfico muestra las diferentes felicitaciones en algunos días significativos para la población en Twitter. _#FelizNavidad_ obtiene un primer puesto muy superior al del resto, seguido de #FelizAño. El podio lo cierra la felicitación del Día de la Madre, aunque ya los datos son muy inferiores a los de los dos primeros _#Hashtags_. 
Los datos se recogen en un **gráfico de barras** en el que se han ordenado los resultados de mayor a menor, facilitando así la comparación de los resultados. Se ha personalizado el estilo del gráfico mediante una selección de colores determinada ya que _Datawrapper_ da un estilo crómático por defecto. Para su elección se ha buscado qué colores se relacionan con cada festividad. Por ejemplo, se ha seleccionado el verde para la Navidad, el amarillo para la Nochevieja o el morado para el Día de la Madre por su relación con la figura femenina. El día del alzamiento se ha dejado en color gris ya que no se trata de una festividad. Sin embargo, se ha mantenido el dato debido a la gran cantidad de _tweets_ sobre el tema. Gracias al uso de los colores se ha conseguido un diseño más atractivo y llamativo que permite al usuario diferenciar unas categorías de otras fácilmente. 

El **gráfico de barras** se erige como uno de los más completos en cuanto a información. Este ofrece un encabezado con etiquetas descriptivas, categorías y valores numéricos que facilitan su comprensión. Este gráfico es, en general, fácil de leer y de entender. En el caso particular de las festividades, el gráfico permite visualizar ocho categorías diferentes de la forma más sencilla posible.
 
![festividad2.png](/img/festividad2.png)

2. Este gráfico refleja la **cantidad de _tweets_ que se pusieron en las dos festividades más felicitadas en Twitter**, **Nochebuena** y **Nochevieja**. A pesar de que a priori se podría pensar que la Nochevieja es más felicitada en Redes Sociales, los resultados de las felicitaciones en _Twitter_ el día de Navidad son sorprendentes. Con el **gráfico circular** el usuario obtiene rápidamente la respuesta sobre qué festividad es más celebrada en la red social. En cuanto al uso de los colores, se han escogido los mismos que en el gráfico anterior por su complementariedad: el verde se asocia con la Navidad, aunque también lo hacen otros colores como el rojo, pero se ha utilizado para otra fiesta. Por su parte, el amarillo se relaciona con la Nochevieja por su semejanza con el dorado, un color que no se encuentra en la paleta de _Datawrapper_.  

Se ha escogido el **gráfico circular** porque es óptimo para mostrar información sobre pocos datos. En concreto, se trabaja con el número de _tweets_ en **Navidad** y el número de _tweets_ en **Año Nuevo**. Estas dos categorías quedan comparadas en el gráfico de forma clara y sencilla. De este modo el usuario obtiene rápidamente la respuesta sobre qué festividad es más celebrada en la red social, en este caso **Nochebuena**.   
