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

- **Heatmaps (Mapas de calor):** [[README#5.e Aplicación del método Eye Tracking|Analizados aquí]]
- **Zonas de Silencio:** La más remarcable es la información de la página principal que se encuentra bajo la imagen de recepción.
- **Hallazgo clave:** Casi ningún usuario trató de hacer scroll en la página principal y los que lo hicieron solo miraron por encima, no prestaron demasiada atención.

## 5. Auditoría de Accesibilidad

Sintetiza el cumplimiento técnico y normativo.

- **Puntuación Automática:** 81% (LightHouse).
- **Principales barreras:** De manera resumida, se encuentran problemas de contraste, falta de texto y falta de etiquetas. [[Acceibility-Report-template#4. Tabla de Hallazgos y Prioridades|Enlace al documento]]

## 6. Conclusiones y Recomendaciones (Actionable Insights)

| **Prioridad** | **Hallazgo**                                                                                                                 | **Recomendación de Mejora**                                |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Media**     | La página principal es demasiado grande y espaciosa, los usuarios parecían no ser capaces de analizar lo que tenían delante. | Compactar más el contenido de la página principal,         |
| **Media**     | La página presenta algunos problemas de cara a la accesibilidad.                                                             | Abordarlos y solucionarlos uno a uno para pulir la página. |
