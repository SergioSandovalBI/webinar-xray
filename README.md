# WEBINAR X-Ray 🎓

<p align="center">
<img src="https://bootcamp-institute.com/cdn/shop/files/Bootcamp-Institute_Aprende-Cloud-computing-con-los-expertos.jpg?v=1650398319" alt="Logo" width="200" height="100">
</p>

Bienvenido al repositorio oficial del **Webinar X-Ray**, impartido por **[Sergio Sandoval](https://www.linkedin.com/in/sergioaugustosandoval)**, administrador de sistemas en la nube de AWS (SysOps).

## Objetivo del webinar 🎯

El objetivo de este webinar es capacitarte para utilizar eficazmente AWS X-Ray y así mejorar la observabilidad de tus aplicaciones distribuidas en la nube. A través de ejemplos prácticos, descubre cómo monitorear el rendimiento, identificar y solucionar problemas de manera eficiente, y optimizar el uso de recursos en tus aplicaciones.

## ¿Qué Aprenderás? 📚

- Utilizar AWS X-Ray para monitorear y mejorar el rendimiento de aplicaciones en la nube.
- Identificar y solucionar problemas de manera eficiente en aplicaciones distribuidas.
- Utilizar los datos de X-Ray para mejorar la escalabilidad y la disponibilidad de sus aplicaciones.
- Obtener información sobre cómo X-Ray puede ayudarles a optimizar los costos de sus aplicaciones en la nube.

## Requisitos ✅

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos:

- Una aplicación instalada y funcional en una cuenta de AWS.
- Acceso a esa cuenta con los permisos necesarios para usar Amazon X-Ray.
- Conocimientos básicos en el uso de la consola y CLI.

## Instrucciones 🚀

Para realizar lo visto en el webinar, sigue estos pasos:

**Recomendación:** seguir estas instrucciones acompañado del video del webinar *(disponible aquí el viernes 5 de abril en la mañana)*, donde hay más detalles y explicaciones.

### Interacción en consola

1.	Abrir la aplicación (previamente instalada y ejecutada en la cuenta de AWS) y realizar varias interacciones y/o consultas.
2.	Ingresar a la consola de la cuenta de AWS donde está instalada la aplicación. 
3.	Ingresar al servicio **CloudWatch** y a continuación desplegar la opción **Rastros de X-Ray** que se encuentra en el menú principal lateral izquierdo.
4.	Ingresar a la opción **Rastros.**
***Nota:*** *para poder ver las métricas de la aplicación en X-Ray, se debe asegurar que está en la misma región en que fue instalada la aplicación.*
5.	En la parte superior derecha de la página principal **Trazas,** hay una barra horizontal que muestra las opciones: **5m – 15m – 30m – 1h – 3h – 6h – Personalizado.** Esas opciones representan el período de tiempo de las trazas que se desean mostrar desde que se crearon cuando se realizaron las interacciones con la aplicación. Escoger la opción **5m.** Tener en cuenta que, al pasar 5 minutos, esas opciones ya no se mostrarán, por lo cual se debe escoger un período de tiempo más largo para que se muestren de nuevo.
6.	Más abajo, en la sección **Refinadores de consultas,** la opción **Ajustar consulta por** es una lista desplegable donde se encuentran varias opciones de consulta que mostrará los resultados en un listado más abajo. Dejar la opción **Nodo** que está actualmente.
7.	El listado de **Nodos,** que se menciona en el punto anterior, muestra los nodos a los que pertenecen las trazas consultadas. Escoger uno o varios nodos del listado, hacer clic en el botón **Agregar a consulta** que se encuentra en la parte superior derecha del listado, lo cual agrega esa consulta en un campo de búsqueda de trazas que está debajo de la barra horizontal de tiempo que se menciona en el punto 5, hacer clic en el botón **Ejecutar consulta** y mostrará solo las trazas del nodo o los nodos escogidos.
8.	Las trazas se muestran en una tabla que se encuentra en la parte inferior de la página. En esta tabla se muestran todas las trazas, cuando se escoge el período de tiempo o cuando se realiza una búsqueda específica, como por ejemplo la búsqueda que se realizó en el punto anterior.
9.	En el menú principal lateral izquierdo, ingresar a la opción **Mapa de registros de seguimiento** en la misma opción desplegable **Rastros de X-Ray.**
10.	En la página principal llamada **Trace Map (Mapa de trazas),** se muestra un gráfico de **Nodos (círculos)** unidos por líneas. Ese gráfico representa la interacción del cliente con la aplicación y de la aplicación con los servicios de AWS. El gráfico muestra las trazas que se han consultado por período de tiempo en la barra horizontal superior.
11.	Al seleccionar un nodo, aparece una información en un cuadro llamado **Leyenda y opciones,** en la parte derecha del gráfico. En ese cuadro se encuentra información que ayuda a entender los nodos y la información que aparece en cada uno de ellos en el gráfico.
12.	Dentro de ese cuadro hay una opción que se llama **Mostrar en nodos,** donde se puede escoger entre **Métricas** e **Iconos,** así cambia la información que se muestra en cada nodo en el gráfico.
13.	Al seleccionar un nodo, debajo del gráfico se habilita una opción desplegable con el nombre del nodo. Al desplegar esa opción muestra diferentes tipos de información y gráficos de métricas que son muy útiles para saber cómo se comporta el nodo y que información contiene. Siéntase libre de interactuar con ese panel y descubrir más información y métricas.
14.	Regresar a la opción **Rastros** en el menú principal lateral izquierdo.
15.	En la tabla **Trazas,** que se encuentra en la parte final de la página, hacer clic en el **ID** de cualquier traza, que se encuentra en la primera columna de la tabla.
16.	En la parte superior de la página se encuentra la siguiente información: **ID de la traza, método HTTP, código de respuesta HTTP, duración la acción y tiempo en que fue ejecutada la acción.**
17.	En la sección **Detalle de la traza** se encuentra un gráfico de los nodos que interactúan con la traza consultada. Este gráfico funciona y muestra información de la misma manera que lo descrito en los puntos anteriores.
18.	Un poco más abajo, en la sección **Línea temporal de los segmentos,** se encuentran los **segmentos,** que representan cada unidad de trabajo, y los **subsegmentos** que son las acciones realizadas en cada una de esas unidades.
19.	En esa tabla de línea temporal se encuentra información importante como la duración de la acción, el código de respuesta y una línea de tiempo gráfica con el nombre de la acción y la duración de cada una.
20.	Al seleccionar cada una de las acciones, se abre una sección llamada **Detalles del segmento,** donde se encuentra en detalle toda la información perteneciente a esa acción.


### Interacción en CLI

1.	Ingresar al servicio **CloudShell.** Se puede ingresar desde la opción que se encuentra en la esquina inferior izquierda de la ventana o abriéndolo como cualquier otro servicio de AWS. Si desea también puede usar el CLI desde el equipo local ingresando la información necesaria para conectarse a la cuenta de AWS donde se encuentra la aplicación.
2.	Ingresar el siguiente commando:

```
aws xray get-trace-summaries --start-time 2024-04-03T15:10:00-05:00 --end-time 2024-04-03T15:15:59-05:00 --region us-east-1 --output json

```

Reemplazar los datos de **región (--region), fecha y tiempo (--start-time --end-time)** acorde al ejercicio actual. También se puede cambiar el formato de **entrega (--output)** json por las opciones table o text. Este comando entrega una lista, en formato json, de las trazas que están disponibles en el período de tiempo y región definidos. Explorar cuántas trazas y que información de cada traza se muestra.

3.	Copiar el **ID** de una de las trazas y guardarlo en un bloc de notas.
   
4.	Ingresar el siguiente commando:

```
aws xray get-trace-graph --trace-ids 1-660dbff1-29799005761ba9c76f2d67b4 --region us-east-1 --output json
```

Reemplazar el dato de **región (--region)** acorde al ejercicio actual. También se puede cambiar el formato de **entrega (--output)** json por las opciones table o text. Reemplazar el **ID de traza (--trace-ids)** del comando por el **ID** copiado en el bloc de notas. Este comando entrega información detallada de la traza consultada, como segmentos, subsegmentos, latencia, etc. Explorar que otra información de la traza se muestra.

5.	Una buena práctica para entender mejor las consultas en CLI, es hacerlo al mismo tiempo en la consola, para comparar la información y los resultados de las consultas.

💡 **Consejo:** Explora y experimenta con las diferentes opciones y herramientas que ofrece Amazon X-Ray para obtener una comprensión profunda de cómo se comportan tus aplicaciones en AWS. Utiliza estas instrucciones como guía inicial, pero no dudes en profundizar en las características específicas que pueden ser más relevantes para tus necesidades.

## Recursos Adicionales 🛠️

- [Guía de usuario de Amazon X-Ray](https://docs.aws.amazon.com/es_es/xray/latest/devguide/aws-xray.html)
- [AWS re:Invent 2018: Deep Dive into AWS X-Ray: Monitor Modern Applications](https://www.youtube.com/watch?v=5MQkX57eTh8)

## Conéctate con Bootcamp Institute 🌐

Queremos que seas parte de nuestra creciente comunidad. Sigue nuestras redes sociales y mantente actualizado con las últimas noticias, cursos y eventos de Bootcamp Institute.

- **Página Web:** [Visita nuestra página](https://bootcamp-institute.com/) <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQVDd5yWRGNNxHId-np7B31fLaWFtbUPkVZ-CJXc8oUJQ&s" alt="Web" width="20" height="20">
- **Instagram:** [@bootcampinstitute](https://www.instagram.com/bootcamp_institute/) <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/2048px-Instagram_logo_2016.svg.png" alt="Instagram" width="20" height="20">
- **LinkedIn:** [Bootcamp Institute](https://www.linkedin.com/company/bootcamp-institute) <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/LinkedIn_icon.svg/2048px-LinkedIn_icon.svg.png" alt="LinkedIn" width="20" height="20">
- **Facebook:** [Bootcamp Institute](https://www.facebook.com/bootcampinstituteLATAM/) <img src="https://upload.wikimedia.org/wikipedia/commons/b/b9/2023_Facebook_icon.svg" alt="Facebook" width="20" height="20">
- **WhatsApp:** [Pregunta por Whatsapp](https://api.whatsapp.com/send?phone=525567474611&text=Hola,%20me%20gustar%C3%ADa%20recibir%20m%C3%A1s%20informaci%C3%B3n%20sobre%20su%20oferta%20educativa.) <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/WhatsApp.svg/2044px-WhatsApp.svg.png" alt="WhatsApp" width="20" height="20">

## ¿Tienes Preguntas? 🤔

Si tienes preguntas o necesitas asistencia, no dudes en contactar al instructor del curso o a nuestro equipo de soporte en **<operaciones@bootcamp.institute>**.

## Contribuir 💡

Este repositorio está abierto a contribuciones. Si tienes ideas para mejorar el material del curso o deseas añadir recursos adicionales, por favor lee nuestra guía de contribución.

---

¡Gracias por ser parte del **Webinar X-Ray** en **Bootcamp Institute**! Estamos emocionados de verte crecer en tu carrera profesional. 💼🚀
