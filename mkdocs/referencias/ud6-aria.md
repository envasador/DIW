WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) es una especificación técnica desarrollada por el Consorcio World Wide Web (W3C) que busca mejorar la accesibilidad de las aplicaciones y contenidos web, especialmente aquellos dinámicos o interactivos creados con tecnologías como Ajax, HTML y JavaScript[1][2][8].

### Objetivos principales
- **Facilitar la accesibilidad**: Permite a las personas con discapacidades sensoriales, como los usuarios de lectores de pantalla, interactuar con contenido dinámico y controles avanzados de interfaz[2][3].
- **Añadir semántica**: Proporciona roles, propiedades y estados adicionales que describen la función y el comportamiento de los elementos de la interfaz, mejorando su interpretación por herramientas de apoyo[4][7].

### Casos de uso
WAI-ARIA es especialmente útil en:
- Controles avanzados como carruseles, sliders, menús desplegables y modales.
- Áreas dinámicas que actualizan contenido automáticamente, como chats o banners[3][4].
- Elementos personalizados que no tienen equivalentes nativos en HTML, como `<div role="button">` para simular un botón[4].

### Componentes clave
1. **Roles**: Definen la función de un elemento (e.g., `role="navigation"` para menús).
2. **Propiedades y estados**: Indican características dinámicas como si un menú está desplegado o colapsado (`aria-expanded="true/false"`)[3][4].
3. **Regiones vivas**: Notifican cambios automáticos en zonas específicas del contenido para que los usuarios sean informados sin perder el contexto[3].

### Recomendaciones
Aunque WAI-ARIA es poderosa, se recomienda usar primero elementos nativos de HTML antes de recurrir a sus atributos. Además, una implementación incorrecta puede perjudicar la accesibilidad en lugar de mejorarla[4].

Fuentes
[1] WAI ARIA SEO Accesible - SEO-onpage - Ricard Menor https://www.seofreelance.es/wai-aria-seo-accesible/
[2] WAI-ARIA. Accesibilidad Digital - Universidad de Alicante https://web.ua.es/es/accesibilidad/accesibilidad-web/wai-aria.html
[3] WAI-ARIA. Introducción, referencias, ejemplos, herramientas https://olgacarreras.blogspot.com/2007/09/wai-aria-introduccion-referencias.html
[4] WAI-ARIA | Guía rápida de accesibilidad web https://accesible.es/wai-aria
[5] ¿Qué tienes que saber de la wai-aria para validar accesibilidad? https://elminimoviable.es/que-tienes-que-saber-de-la-wai-aria-para-validar-accesibilidad/
[6] WAI-ARIA, una aproximación - No Solo Usabilidad https://www.nosolousabilidad.com/articulos/wai_aria.htm
[7] ¿Qué son los Roles de WAI-ARIA y para qué sirven? - LinkedIn https://es.linkedin.com/pulse/qu%C3%A9-son-los-roles-de-wai-aria-y-para-sirven-accessibilitycl-jnuhc
[8] WAI-ARIA https://en.wikipedia.org/wiki/WAI-ARIA
