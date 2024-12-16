---
hide:
  - navigation
---

# **Proyecto 4: Testing en producción
---

## 1.Instrucciones
Las siguientes indicaciones de entrega servirán para todas las entregas de este módulo.

- El contenido de la actividad estará recogido en un archivo **PDF** con el nombre:  
  `diw.nombre-practica.nombre.apellido.pdf`
    - `diw`: Siglas del módulo
    - `Nombre de la práctica`
    - `Nombre del alumno/a`
    - `Apellidos del alumno/a`
- El nombre del documento **no debe contener acentos**.
- Ejemplo: Si la práctica es de prototipado web y la alumna es **Viana Fernández**, el nombre del archivo será:  
  `diw.practica-prototipado-web.viana.fernandez.pdf`

### Requisitos del documento:
- Debe estar **bien presentado**, sin faltas de ortografía y con una estética adecuada.
- Los nombres y apellidos de los alumnos/as deben aparecer dentro del documento.
- Fuentes de información de Internet deben incluir la **URL** correspondiente.

### Plagio
- El plagio resultará en una **calificación de 0** tanto para quien copia como para quien cede la tarea.
- El **Resultado de Aprendizaje** relacionado también será calificado con **0**.

### Entrega
- El archivo se subirá a través de la **plataforma Moodle** en la tarea correspondiente.
- Cada alumno/a debe subir su propia copia del archivo, incluso si se ha realizado de forma grupal.

---

## 2.Objetivos
- Reconocer la **importancia del uso de estándares** en la creación de documentos.
- Verificar la **facilidad de navegación** y **usabilidad** de una página web.
- Utilizar herramientas y técnicas para realizar **tests de usabilidad** en diferentes dispositivos y navegadores.
- Evaluar la **usabilidad** y accesibilidad del interfaz web en entornos de producción.

---

## 3.Resultados de aprendizaje y Criterios de evaluación
**RA6**: Desarrolla interfaces web amigables analizando y aplicando las pautas de usabilidad.
- **CE.c)** Se ha valorado la importancia del uso de estándares en la creación de documentos Web.
- **CE.d)** Se ha verificado la facilidad de navegación de un documento Web mediante distintos periféricos.
- **CE.f)** Se ha verificado la usabilidad del interfaz Web creado en diferentes navegadores y tecnologías.

---

## 4.Prueba

### Testing de Usabilidad de una Web
Una vez desarrollado el proyecto web, se realizará un **testing de usabilidad** para evaluar la interfaz. La prueba debe ser visible a través de una **URL** (por ejemplo, **GitHub Pages** o servidor propio).

### Proceso de la Práctica

1. **Evaluación inicial de estándares y navegación**
    - Elige un proyecto web propio o de un/a compañero/a.
    - Analiza los **estándares empleados** en el desarrollo:
        - ¿Qué estándares se han aplicado correctamente?
        - ¿Cuáles no cumplen con las pautas de usabilidad?
    - Evalúa la **facilidad de navegación** del sitio web con diferentes periféricos (ratón, teclado, pantalla táctil).
    - Realiza una reflexión final sobre la importancia de los estándares y la navegación intuitiva.

2. **Pruebas de usabilidad y velocidad con herramientas automáticas**
    - Utiliza las siguientes herramientas para evaluar la **usabilidad y rendimiento** del sitio web:

1. **[WebPageTest](https://webpagetest.org)**:  
   1.1. Realiza el test en al menos **2 navegadores diferentes** (home).  
   1.2. Evalúa la **navegación** en al menos **2 dispositivos** (listado y producto).

2. **[PageSpeed Insights](https://pagespeed.web.dev/)**:  
   2.1. Analiza al menos **3 páginas clave**: home, listado y producto.  
   2.2. Identifica los **elementos de mejora** y explica las recomendaciones.

3. **Optimización con Lighthouse**:  
   3.1. Evalúa el rendimiento del sitio web utilizando **Lighthouse** en Chrome DevTools. Mide y analiza los siguientes parámetros:
    - **Largest Contentful Paint (LCP):** tiempo que tarda en renderizarse el elemento más grande visible.
    - **Interaction to Next Paint (INP):** latencia en la interacción con elementos interactivos.
    - **Cumulative Layout Shift (CLS):** estabilidad visual del contenido durante la carga.
    - **First Contentful Paint (FCP):** tiempo hasta que se muestra el primer elemento visual.
    - **First Input Delay (FID):** tiempo de respuesta a la primera interacción del usuario.
    - **Time to First Byte (TTFB):** tiempo hasta recibir el primer byte del servidor.  
      3.2. Documenta los resultados obtenidos y realiza recomendaciones específicas para optimizar cada parámetro medido.

3. **Testing de usabilidad manual con usuarios reales**
    - Diseña un breve **test de usabilidad** donde los usuarios realicen las siguientes tareas:
        - Encontrar información específica en el sitio web (por ejemplo, localizar el apartado de contacto o una sección de productos).
        - Completar una acción común (como rellenar un formulario de registro con datos ficticios o agregar un producto al carrito).
    - Documenta la experiencia del usuario:
        - Problemas encontrados (como enlaces rotos, dificultad en la navegación, etc.).
        - Tiempo necesario para completar las tareas.
        - Comentarios o sugerencias sobre la facilidad de uso y diseño de la interfaz.

4. **Evaluación con Ghost Inspector**
    - Realiza un testeo automatizado con **Ghost Inspector** para comprobar la navegación general y los procesos críticos del sitio web.
    - Adjunta el **video generado** y analiza los resultados. Por ejemplo, presta atención a posibles fallos como botones inactivos, enlaces rotos o tiempos de carga excesivos.
    - Una guía visual sencilla podría consistir en comparar la salida del testeo con el comportamiento esperado (por ejemplo, verificar si los pasos automatizados coinciden con el flujo de navegación diseñado).

---

## 5.Entrega Final
Debéis entregar:
- **Documento en PDF** con el informe completo, que incluya:
    - Evaluación de estándares y navegación.
    - Resultados de los tests automáticos (WebPageTest, PageSpeed Insights y accesibilidad).
    - Resultados del test de usabilidad manual.
    - Resultados del test con Ghost Inspector.
    - Reflexiones finales sobre la **usabilidad** y navegación del sitio web.
- **Archivos generados** necesarios para la justificación.

**¡Ánimo! 🖖**

---

### Anexo: Herramientas Recomendadas
- **WebPageTest**: [https://webpagetest.org](https://webpagetest.org)
- **PageSpeed Insights**: [https://pagespeed.web.dev/](https://pagespeed.web.dev/)
- **WAVE**: [https://wave.webaim.org](https://wave.webaim.org)
- **Lighthouse**: Disponible en Chrome DevTools.
- **Ghost Inspector**: [https://ghostinspector.com](https://ghostinspector.com)  


## 6.Rúbrica de Evaluación

### **Criterio CE.c: Valoración de estándares en la creación de documentos Web**
| Nivel | Descripción                                                                 |
|-------|-----------------------------------------------------------------------------|
| 10    | Identifica y aplica correctamente todos los estándares.                     |
| 8     | Identifica la mayoría de los estándares con algunas aplicaciones erróneas. |
| 6     | Reconoce algunos estándares, pero con errores frecuentes en su aplicación. |
| 4     | Muestra un conocimiento muy limitado de los estándares aplicados.          |
| 0     | No identifica ni aplica los estándares requeridos.                         |

### **Criterio CE.d: Verificación de la facilidad de navegación con distintos periféricos**
| Nivel | Descripción                                                                 |
|-------|-----------------------------------------------------------------------------|
| 10    | Comprueba exhaustivamente la navegación con distintos periféricos y reporta resultados claros. |
| 8     | Realiza pruebas en la mayoría de periféricos, con resultados satisfactorios. |
| 6     | Pruebas parciales y con documentación limitada.                             |
| 4     | Pruebas mínimas y resultados poco documentados.                             |
| 0     | No realiza pruebas con periféricos.                                         |


