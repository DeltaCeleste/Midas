# Usability Report



<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRF017nhV-TFmNER2OM8UbXtdN6xwAKBYrv0i6onNfKu6Yn0BV0RK6aiOroeXl73LSY-B0&usqp=CAU" alt="usability Download png" style="height:150px" />

### Evaluación de usabilidad del proyecto Graná en Grado

Fecha: 28/06/2026

![img Proyecto](P5/UsabilityReport/LogoCafeteria.png)

[Enlace a GITHUB del proyecto](https://github.com/maximartinm/UX_CaseStudy)

### Realizado por:  

Informe realizado por el equipo DIU1-Midas

Su estilo espacioso y poco cargado hace la navegación rápida y accesible si sabes donde mirar, sin embargo, ese sentimiento de espacio puede provocar una distracción en los elementos existente que tienden a destacar en el contraste del vacío. Esto puede ser una gran fortaleza si los elementos mostrados son los que se buscan, pero si no, puede llevar a perdidas de tiempo para algunos usuarios que focalicen su atención donde no deben.


## 1 RESUMEN EJECUTIVO  (Executive Summary)

- **Objetivo:** Evaluamos la usabilidad de la página para su uso por un público general de cara a lanzarla
- **Metodología:** A/B testing de dos pruebas seguido de un test SUS y realizando un eye tracking mientras el usuario realizaba las pruebas.
- **Principales Hallazgos:** su estilo abierto y espacioso provoca dispersiones de atención o focalizaciones en elementos que no tienen porque ser los deseados.
- **Resultado Global:** Puntuación SUS media de **86,25**, lo que lo posiciona como decentemente aceptable pero con algo de margen de mejora.


## 2. Metodología y Reclutamiento

- **Perfil de los participantes:** Se han buscando perfiles distintos, centrándonos en especial en grupos con diferentes niveles de experiencia con Tecnologías Informáticas.
- **Escenario de la prueba:** Los usuarios realizaron dos pruebas, buscar acceder a la carta del sitio e iniciar sesion/realizar pedido.
- **Herramientas:** GazeMapping, Tally, Wave, Web Disability Simulator y Lighthouse Accessibility.

## 3. Resultados del Cuestionario SUS (Datos Cuantitativos)

- **Comparativa A vs. B:** ![Diagrama](P5/UsabilityReport/barras.png)
Nuestro caso A ha obtenido una mejor puntuación media, aunque la diferencia tampoco es demasiado grande.
- **Desglose por ítems:** Las preguntas del test SUS dieron un rendimiento bastante parejo, la más destacable podría ser la pregunta 10, que es la única que ha obtenido un 3, aunque esto puede deberse al rango de edad y experiencia TIC concreto.

Valoración numérica del SUS - **86,25**


## 4. Análisis de Eye Tracking (Datos Biométricos)

- **Heatmaps (Mapas de calor):** 
	- Prueba 1:
![landing page](P5/B/analisis_sitio10.jpg)
![landing page](P5/B/analisis_sitio12.jpg)
	Para este caso, los usuarios tampoco presentaron mayores dificultados ya que también era de fácil acceso. Lo más destacable que revela el mapa de calor es que, pese a tener los cafés también en la página principal, debido al tamaño de la página, no todos los usuarios bajaron lo suficiente como para encontrarlos (incluso hubo quien bajó pero no le dio importancia y se metió igualmente por el enlace sin saber que los había localizado).
	- Prueba 2:
![landing page](P5/B/analisis_sitio11.jpg)
	En este caso tampoco ha habido problema. Siendo la segunda prueba de esta página, los usuarios han ido más a tiro hecho. Además la página del carrito esta muy bien condensada.
	
- **Zonas de Silencio:** La más remarcable es la información de la página principal que se encuentra bajo la imagen de recepción.
- **Hallazgo clave:** Casi ningún usuario trató de hacer scroll en la página principal y los que lo hicieron solo miraron por encima, no prestaron demasiada atención.

## 5. Auditoría de Accesibilidad

Sintetiza el cumplimiento técnico y normativo.

- **Puntuación Automática:** 81% (LightHouse).
- **Principales barreras:** De manera resumida, se encuentran problemas de contraste, falta de texto y falta de etiquetas. 

| **ID**     | **Prioridad** | **Criterio WCAG**               | **Error detectado**                                                                                          | **Recomendación Técnica**                                                                                             |
| :--------- | :------------ | :------------------------------ | :----------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------- |
| **ACC-01** | **Crítica**   | 3.3.2 Etiquetas o instrucciones | Falta de etiqueta en el cuadro de búsqueda superior                                                          | Añadir el atributo `aria-label="Buscar en el catálogo de cafés"`                                                      |
| **ACC-02** | **Alta**      | 1.4.3 Contraste mínimo          | 6 errores de contraste de los productos sobre el fondo crema.                                                | Cambiar el color a un tono oscuro de alta legibilidad                                                                 |
| **ACC-03** | **Alta**      | 1.1.1 Contenido no textual      | Ausencia de textos alternativos funcionales en las imágenes principales del catálogo.                        | Implementar el atributo `alt=""` explícito en imágenes decorativas o descripciones funcionales si aportan contexto    |
| **ACC-04** | **Media**     | 4.1.2 Nombre, función, valor    | Atributos `id` duplicados (repetidos en las tarjetas de productos de la cuadrícula del catálogo).            | Eliminar los `id` repetitivos y crear nuevos                                                                          |
| **ACC-05** | **Media**     | 2.4.7 Foco visible              | El indicador de foco (`:focus`) está invisible o suprimido al tabular por los botones y enlaces.             | Implementar en el CSS global un estilo visual claro con `outline` para resaltar el elemento interactivo activo.       |
| **ACC-06** | **Media**     | 2.4.3 Orden del foco            | Orden de tabulación incoherente al navegar con teclado por los elementos interactivos del Footer y catálogo. | Asegurar el flujo lógico nativo del DOM y evitar el uso de atributos `tabindex` con valores positivos mayores a cero. |


## 6. Conclusiones y Recomendaciones (Actionable Insights)

| **Prioridad** | **Hallazgo**                                                                                                                 | **Recomendación de Mejora**                                |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Media**     | La página principal es demasiado grande y espaciosa, los usuarios parecían no ser capaces de analizar lo que tenían delante. | Compactar más el contenido de la página principal,         |
| **Media**     | La página presenta algunos problemas de cara a la accesibilidad.                                                             | Abordarlos y solucionarlos uno a uno para pulir la página. |
