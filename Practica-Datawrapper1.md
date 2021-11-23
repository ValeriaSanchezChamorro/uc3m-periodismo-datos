# ¿Qué se festeja más en Twitter?

A partir de los datos del **proyecto TRESCA** vertidos en _GitHub_, se han realizado dos gráficos basados en algunos aspectos relevantes relacionados con las festividades en Twitter. Para obtener los resultados finales, se ha trabajado con tres programas diferentes: _OpenRefine_, _Excel_ y _Datawrapper_.

Entre los diferentes #Hashtags que se proponían se ha decidido escoger aquellos que aparecen en tweets más de 10.000 veces para trabajar con los datos de forma más sencilla. 

## Trabajando con los datos

La primera dificultad que se ha encontrado reside en que los datos con los que se ha trabajado no representan la realidad en su totalidad. Todos aquellos días en los que los Hashtags no han superado los 10.000 tweets no son contabilizados en el CSV. Por lo tanto, las informaciones con las que se cuenta son una estimación de la realidad. 

Para la creación de los gráficos se ha procedido a escoger un período de tiempo delimitado. El año 2020 se presentaba más interesante en cuanto a cantidad de Tweets a pesar del tramo sin informaciones de los meses de verano. Para trabajar con estos datos se ha creado una **faceta temporal** y se ha seleccionado este intervalo de tiempo (enero 2020 – diciembre 2020). Además, se evita contar con los datos de 2020 y 2021 de las mismas celebraciones. 

![cluster.png](/img/cluster.png)

Una vez delimitado este aspecto, se ha procedido a eliminar las celdas vacías que no contenían el total de #Hashtags. Para ello se ha creado una **nueva faceta personalizada para celdas nulas** que separa filas en blanco y filas con datos. Después se han eliminado aquellas celdas vacías. 

Ya eliminadas las celdas vacías, se ha utilizado la función **Cluster** para agrupar aquellos #Hashtags que tratan de la misma temática y que varían solamente en algunos caracteres (por ejemplo, _#Feliz Dia de Navidad_ y _#FelizNavidad_). En la columna dedicada a los nombres de los Hashtags, se ha usado la herramienta de **Editar texto**. Con ella se han cambiado varios caracteres de algunos tweets para conseguir un objetivo similar al de Cluster. Por ejemplo, se ha editado el nombre de la etiqueta _Feliz Fin de Año_ para que sea igual a _FelizAño_. Este cambio se ha aplicado a toda la columna con la que se ha trabajado. 

![editar.png](/img/editar.png)

Por último, se ha utilizado Excel para sumar el número total de _#Hastags_ en el período de tiempo de un año (2020). Gracias a la fórmula numérica **=SUMAR.SI** se han contabilizado los resultados totales de los ocho días más felicitados en Twitter:

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

