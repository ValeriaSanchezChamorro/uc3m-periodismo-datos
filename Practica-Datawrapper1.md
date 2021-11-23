# ¿Qué se festeja más en Twitter?

A partir de los datos del **proyecto TRESCA** vertidos en el documento CSV _feliz.csv_ se han realizado dos gráficos relacionados con la felicitación de determinadas celebraciones en Twitter. Para obtener los resultados finales se ha limpiado, operado y ordenado la información del CSV mediante _OpenRefine_ y _Excel_. Finalmente se han trasladado los datos a _Datawrapper_ para conseguir las representaciones gráficas.  

## Trabajando con los datos

La primera dificultad que se ha encontrado reside en que los datos con los que se ha trabajado no representan la realidad en su totalidad. Todos aquellos días en los que los _#Hashtags_ no han superado los 10.000 tweets no son contabilizados en el CSV. Por lo tanto, las informaciones con las que se cuenta son una estimación de la realidad. 

Para la creación de los gráficos se ha escogido un período de tiempo delimitado. El año 2020 resulta más interesante en cuanto a cantidad de Tweets a pesar del tramo sin informaciones de los meses de verano, dado que el mes de diciembre es especialmente activo en Twitter. Para trabajar con estos datos se ha creado una **faceta temporal** y se ha seleccionado este intervalo de tiempo (marzo 2020 – diciembre 2020). De este modo también se evita contar con los datos de 2020 y 2021 sobre las mismas festividades dos veces.  

![cluster.png](/img/cluster.png)

Después se ha procedido a eliminar las celdas vacías que no contenían el total de _#Hashtags_. Para ello se ha creado una **nueva faceta personalizada para celdas nulas** que separa filas en blanco y filas con datos. Después se han eliminado aquellas celdas vacías. 

Una vez eliminadas se ha utilizado la función **Cluster** para agrupar aquellos _#Hashtags_ que tratan la misma temática y que varían solamente en algunos caracteres (por ejemplo, _#Feliz Dia de Navidad_ y _#FelizNavidad_). En la columna dedicada a los nombres de los _#Hashtags_ se ha usado la herramienta de **Editar texto**. Con ella se han cambiado varios caracteres de algunos tweets. Por ejemplo, se ha editado el nombre de la etiqueta _Feliz Año_ para que el _#Hashtag_ no tenga espaciado (#FelizAño). Este cambio se ha aplicado a toda la columna con la que se ha trabajado. 

![editar.png](/img/editar.png)

Por último, se ha utilizado Excel para sumar el número total de _#Hashtags_ en el período de tiempo de un año (2020). Gracias a la fórmula numérica **=SUMAR.SI** se han contabilizado los resultados totales de los ocho días más felicitados en Twitter:

-	FelizNavidad
-	FelizAño 
-	FelizDiadeLaMadre
-	FelizDiaDelPadre
-	FelizAlzamiento
-	Feliz Halloween
-	FelizDiaDelTrabajador
-	Feliz Pascua

## Representación gráfica

Para la creación de los gráficos se ha utilizado tanto la academia de Datawrapper como el catálogo de la visualización de datos. 

![festividad1.png](/img/festividad1.png)

![festividad2.png](/img/festividad2.png)

