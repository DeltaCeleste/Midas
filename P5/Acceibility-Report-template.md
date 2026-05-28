# Accesibility Report (template)

<img src="https://img.uxcel.com/cdn-cgi/image/format=auto/practices/wcag-principles-overview-1742315821212/a-1742315821212-2x.jpg" alt="usability Download png" style="height:200px" />

## 1. Ficha Técnica del Informe

Antes de entrar en detalles, define el alcance.

- **Nombre del proyecto:** Graná en Grano
- **Normativa de referencia:** WCAG 2.1 o 2.2 (Nivel AA).
- **Herramientas utilizadas:** WAVE, Web Disability Simulator
- **Fecha de la auditoría:** 28/05/2026



NOTA: El marco normativo para la web, el estándar es el **WCAG (Web Content Accessibility Guidelines)**.

- **Nivel de conformidad:** **AA y A** (el estándar legal para sitios públicos y empresas), Versión  **WCAG 2.2**. Referencia: norma **UNE-EN 301549** 



## 2. Puntuaciones Globales (Métricas Automáticas)
Tras analizar técnicamente las métricas de diagnóstico aportadas, el sitio web presenta un estado de accesibilidad calificado como **Rango Medio (Necesita Mejora)**, obteniendo una puntuación automatizada del **81%** en la auditoría de Google Lighthouse. 

Si bien cuenta con una base de desarrollo sólida reflejada en un **96% en Prácticas Recomendadas** y un **89% en Rendimiento**, la nota específica de accesibilidad se ve penalizada por fallos de diseño visual y estructural confirmados por la herramienta WAVE, la cual detectó un total de **2 errores críticos**, **6 errores de contraste de color** y **14 alertas de usabilidad**.

## 3. Análisis por Principios (POUR)
# Informe de Auditoría de Accesibilidad Web

* **Sitio Web:** Graná en Grano (Prototipo en Figma / Sitio de Cafetería de Especialidad)
* **Fecha de Evaluación:** 28 de mayo de 2026
* **Metodología:** Análisis cruzado basado en los Principios POUR (WCAG 2.1 / 2.2) mediante el uso de herramientas automáticas de diagnóstico (Google Lighthouse y WAVE Web Accessibility Evaluation Tool).

---

## Valoración General de Accesibilidad

En general, presente un buen nivel en cuanto a Prácticas Recomendadas y Rendimiento. En accesibilidad necesita mejoras importantes en cuánto al contraste y marcado, y además el SEO tiene una calificación crítica ya que no hace uso de prácticamente nada que potencie esto, como podría ser técnicas de indexación y uso de metadatos.

### Resumen de Métricas (Google Lighthouse)

| Categoría de Auditoría | Puntuación | Estado Diagnóstico |
| :--- | :---: | :--- |
| **Prácticas Recomendadas (Best Practices)** | `96%` | 🟢 Excelente. El entorno es seguro y sigue los estándares modernos. |
| **Rendimiento (Performance)** | `89%` | 🟢 Muy Bueno. Tiempos de respuesta y carga inicial eficientes. |
| **Accesibilidad (Accessibility)** | `81%` | 🟠 Necesita Mejora. Presencia de fallos en contraste y marcado semántico. |
| **SEO (Optimización en Buscadores)** | `63%` | 🔴 Bajo / Crítico. Requiere optimización urgente de metadatos e indexación. |

---

## Resultados Agrupados por Principios (POUR)

### A Principio: PERCEPTIBLE
* **Error detectado:** Falta de contraste cromático mínimo en los textos de las insignias de los productos y ausencia de textos alternativos funcionales en imágenes.
* **Criterio WCAG incumplido:** *Criterio de Conformidad 1.4.3 - Contraste mínimo (Nivel AA)* y *Criterio 1.1.1 - Contenido no textual (Nivel A)*.
* **Impacto:** Los 6 errores de contraste marcados por la herramienta WAVE en las etiquetas informativas del catálogo impiden que las personas con baja visión, daltonismo o fatiga visual distingan el contenido con claridad sobre sus respectivos fondos de color.
* **Recomendación de mejora:** Modificar las hojas de estilo (CSS) para que la relación de contraste sea mejor. Se sugiere sustituir los textos claros aplicados sobre fondos crema o amarillos por tonalidades oscuras de alta legibilidad.

### B Principio: OPERABLE
* **Error detectado:** Foco de navegación invisible o suprimido mediante código en el menú principal y en los componentes interactivos de compra.
* **Criterio WCAG incumplido:** *Criterio de Conformidad 2.4.7 - Foco visible (Nivel AA)* y *Criterio 2.4.3 - Orden del foco (Nivel A)*.
* **Impacto:** Un usuario que navega utilizando exclusivamente el teclado (con la tecla Tabulación) o mediante pulsadores de asistencia pierde por completo la noción de en qué elemento de la pantalla se encuentra situado (como los botones repetitivos de *"Añadir"*). Esto imposibilita la finalización autónoma de una compra.
* **Recomendación de mejora:** Definir mediante CSS un estilo claro y visualmente llamativo para el estado activo de selección en enlaces y botones.

### C Principio: ROBUSTO
* **Error detectado:** Falta de etiquetas semánticas explícitas en el cuadro de búsqueda principal.
* **Criterio WCAG incumplido:** Criterio de Conformidad 3.3.2 - Etiquetas o instrucciones (Nivel A)
* **Impacto:** El campo de entrada de datos superior no posee un identificador vinculado en el árbol de accesibilidad. Lo cual dificulta la accesibilidad para personas con discapacidad.
* **Recomendación de mejora:** Enlazar formalmente una etiqueta al cuadro de texto usando el atributo for asociado al id correspondiente.

### D Principio: COMPRENSIBLE
* **Error detectado:** Duplicación de identificadores de elemento (IDs duplicados) en las estructuras modulares de los productos.
* **Criterio WCAG incumplido:** Criterio de Conformidad 4.1.2 - Nombre, función, valor (Nivel A)
* **Impacto:** Al repetirse el ID "añadir" en cada tarjeta del catálogo, el navegador falla al construir las relaciones del Árbol de Accesibilidad. Esto impide que las tecnologías de asistencia determinen programáticamente a qué producto específico pertenece cada botón de compra, afectando la transmisión de su nombre accesible y su valor.
* **Recomendación de mejora:** Garantizar la unicidad absoluta de cada atributo id en todo el documento HTML. Si se requiere heredar el mismo comportamiento o diseño visual para toda la cuadrícula de productos, se deben sustituir los identificadores repetidos.


## 4. Tabla de Hallazgos y Prioridades

| **ID** | **Prioridad** | **Criterio WCAG** | **Error detectado** | **Recomendación Técnica** |
| :--- | :--- | :--- | :--- | :--- |
| **ACC-01** | **Crítica** | 3.3.2 Etiquetas o instrucciones | Falta de etiqueta en el cuadro de búsqueda superior |  Añadir el atributo `aria-label="Buscar en el catálogo de cafés"` |
| **ACC-02** | **Alta** | 1.4.3 Contraste mínimo | 6 errores de contraste de los productos sobre el fondo crema. | Cambiar el color a un tono oscuro de alta legibilidad |
| **ACC-03** | **Alta** | 1.1.1 Contenido no textual | Ausencia de textos alternativos funcionales en las imágenes principales del catálogo. | Implementar el atributo `alt=""` explícito en imágenes decorativas o descripciones funcionales si aportan contexto |
| **ACC-04** | **Media** | 4.1.2 Nombre, función, valor | Atributos `id` duplicados (repetidos en las tarjetas de productos de la cuadrícula del catálogo). | Eliminar los `id` repetitivos y crear nuevos|
| **ACC-05** | **Media** | 2.4.7 Foco visible | El indicador de foco (`:focus`) está invisible o suprimido al tabular por los botones y enlaces. | Implementar en el CSS global un estilo visual claro con `outline` para resaltar el elemento interactivo activo. |
| **ACC-06** | **Media** | 2.4.3 Orden del foco | Orden de tabulación incoherente al navegar con teclado por los elementos interactivos del Footer y catálogo. | Asegurar el flujo lógico nativo del DOM y evitar el uso de atributos `tabindex` con valores positivos mayores a cero. |

## 5. Conclusiones y Declaración de Conformidad


### Estado Actual de Conformidad
El sitio web **no es plenamente accesible y cumple de forma muy parcial con el nivel AA** de las directrices WCAG 2.2. Si bien la auditoría automatizada arroja una puntuación base del `81%` en accesibilidad, la coexistencia de barreras críticas en elementos interactivos (ausencia de foco visible e identificadores duplicados en botones) y la falta de etiquetado en el buscador central generan un impacto directo excluyente, impidiendo que usuarios con discapacidades visuales o motoras naveguen de forma autónoma o completen con éxito procesos esenciales en la interfaz.

### Próximos Pasos (Plan de Acción Inmediato)

Para subsanar las vulnerabilidades detectadas con mayor urgencia y elevar significativamente la puntuación en próximas auditorías, el equipo de desarrollo debe priorizar las siguientes tres acciones inmediatas:

1.  **Inyección de Semántica en Formularios (Prioridad Crítica):** Resolver de manera inmediata el error de *Missing form label* en la barra de búsqueda superior añadiendo un atributo estructurado `aria-label` o una etiqueta formal vinculada, garantizando que el control tenga un nombre accesible e identificable por los lectores de pantalla.
2.  **Corrección de la Paleta de Contraste (Prioridad Alta):** Ajustar las hojas de estilo CSS de las insignias del catálogo (*Novedad, Clásico, Pre-entreno, Resistencia*), oscureciendo el color del texto para superar el umbral de contraste mínimo requerido frente al color de fondo crema de las tarjetas.
3.  **Saneamiento del Marcado HTML e Identificadores (Prioridad Media):** Eliminar la duplicación de atributos `id` en la cuadrícula de productos, migrando todos los selectores de estilo repetitivos a clases CSS (`class="..."`) para asegurar que el Árbol de Accesibilidad procese limpiamente la función, el valor y la identidad única de cada botón de compra.










