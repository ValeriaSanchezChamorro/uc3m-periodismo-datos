# ¿Qué se festeja más en Twitter?

En el presente trabajo se pretende exponer los resultados obtenidos tras el análisis de los datos del **proyecto _TRESCA_**. A partir de las informaciones vertidas en el documento CSV _feliz.csv_ se han realizado dos gráficos relacionados con la felicitación de determinadas celebraciones en Twitter. Para obtener los resultados finales se ha limpiado, operado y ordenado el contenido del CSV mediante _OpenRefine_. Finalmente se han trasladado los datos a _Datawrapper_ para conseguir las representaciones gráficas.  

## Trabajando con los datos

Las Redes Sociales son estructuras de Internet en las que los individuos se relacionan de forma rápida. Además, operan en distintos niveles (uno puede utilizar las redes para relacionarse, pero también para su ámbito profesional). Sin embargo, siempre permiten ese intercambio de informaciones ilimitado. Estas redes se utilizan principalmente para comunicarse, pero también sirven para informarse, entretenerse, compartir contenidos y opiniones o comprar productos, entre muchos otros usos. Desde las Redes Sociales es incluso posible convocar manifestaciones masivas. En definitiva, sirven para casi todo lo que se puede imaginar. 

La primera dificultad que se ha encontrado reside en que los datos con los que se ha trabajado no representan la realidad en su totalidad. Todos aquellos días en los que los _#Hashtags_ no han superado los 10.000 tweets no son contabilizados en el CSV. Por lo tanto, las informaciones con las que se cuenta son una estimación de la realidad. 

Para la creación de los gráficos se ha escogido un período de tiempo delimitado. El año 2020 resulta más interesante en cuanto a cantidad de Tweets a pesar del tramo sin informaciones de los meses de verano, dado que el mes de diciembre es especialmente activo en Twitter. Para trabajar con estos datos se ha creado una **faceta temporal** y se ha seleccionado este intervalo de tiempo (marzo 2020 – diciembre 2020). De este modo también se evita contar con los datos de 2020 y 2021 sobre las mismas festividades dos veces.  

![cluster.png](/img/cluster.png)

Después se ha procedido a eliminar las celdas vacías que no contenían el total de _#Hashtags_. Para ello se ha creado una **nueva faceta personalizada para celdas nulas** que separa filas en blanco y filas con datos. Después se han eliminado aquellas celdas vacías. 

Una vez eliminadas se ha utilizado la función **Cluster** para agrupar aquellos _#Hashtags_ que tratan la misma temática yque varían solamente en algunos caracteres (por ejemplo, _#Feliz Dia de Navidad_ y _#FelizNavidad_). En la columna dedicada a los nombres de los _#Hashtags_ se ha usado la herramienta de **Editar texto**. Con ella se han cambiado varios caracteres de algunos tweets. Por ejemplo, se ha editado el nombre de la etiqueta _Feliz Año_ para que el _#Hashtag_ no tenga espaciado (#FelizAño). Este cambio se ha aplicado a toda la columna con la que se ha trabajado. 

![editar.png](/img/editar.png)

Por último, se ha utilizado la fórmula _row.record.celss ['Numero'].value.sum() para sumar el número total de _#Hashtags_ en el período de tiempo de un año (2020). Gracias a la fórmula numérica y a la aplicación de una faceta de texto sobre la columna de los _#Hasghtags_ se han contabilizado los resultados totales de los ocho días más felicitados en Twitter:

-	FelizNavidad (33.145.172)
-	FelizAño (6.345.842)
-	FelizDiadeLaMadre (683.633)
-	FelizDiaDelPadre (526.645)
-	FelizAlzamiento (480.126)
-	Feliz Halloween (315.544)
-	FelizDiaDelTrabajador (180.599)
-	Feliz Pascua (124.774)

## Representación gráfica

Para la creación de los gráficos se ha utilizado tanto la academia de Datawrapper como el catálogo de la visualización de datos. 

![festividad1.png](/img/festividad1.png)

El siguiente gráfico muestra las diferentes felicitaciones en algunos días significativos para la población en Twitter. _#FelizNavidad_ obtiene un primer puesto muy superior al del resto, seguido de #FelizAño. El podio lo cierra la felicitación del Día de la Madre, aunque ya los datos son muy inferiores a los de los dos primeros _#Hashtags_. 
Los datos se recogen en un gráfico de barras en el que se han ordenado los resultados de mayor a menor, facilitando así la comparación de los resultados. Se ha personalizado el estilo del gráfico mediante una selección de colores determinada. Para su elección se ha buscado qué colores se relacionan con cada festividad. Por ello, se ha seleccionado el verde para la Navidad, el amarillo para la Nochevieja por su semejanza con el dorado o el morado para el Día de la Madre por su relación con la figura femenina. El día del alzamiento se ha dejado en color gris porque no se trata de una festividad. Sin embargo, se ha mantenido el dato debido a la gran cantidad de tweets sobre el tema. Asimismo, se consigue un diseño más atractivo y llamativo que permite al usuario diferenciar unas categorías de otras fácilmente. 

Se ha elegido el gráfico de barras es uno de los más completos en cuanto a información (encabezado con etiquetas descriptivas, categorías y valores numéricos). Además, se trata de un tipo de gráfico fácil de leer y de entender. 
 
![festividad2.png](/img/festividad2.png)

El segundo gráfico refleja la cantidad de tweets que se pusieron en las dos festividades más felicitadas en Twitter, **Nochebuena** y **Nochevieja**. A pesar de que a priori se podría pensar que la Nochevieja es más felicitada en Redes Sociales, los resultados de las felicitaciones en Twitter el día de Navidad son sorprendentes. Con el gráfico circular el usuario obtiene rápidamente la respuesta sobre qué festividad es más celebrada en la red social. En cuanto al uso de los colores, se han escogido los mismos que en el gráfico anterior por su complementariedad. 

Se ha escogido el gráfico circular porque es óptimo para mostrar información sobre pocos datos. 
