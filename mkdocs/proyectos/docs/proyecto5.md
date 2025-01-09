
---

## **Mejorando la Accesibilidad Web según WCAG 2.2 Nivel AA**

### **Objetivos**
1. Evaluar y mejorar la accesibilidad del sitio web según las pautas WCAG 2.2, nivel AA.
2. Aplicar técnicas de desarrollo accesible para garantizar una experiencia inclusiva.
3. Utilizar herramientas automáticas y manuales para identificar y corregir barreras de accesibilidad.

---

### **Fases del Proyecto**

#### **Fase 1: Testeo inicial de accesibilidad**
1. **Herramientas de evaluación**:
    - Ejecutar pruebas automáticas con:
        - **Lighthouse** (DevTools en Chrome/Edge).
        - **Wave** (extensión para navegadores o versión web).
        - **Axe** (integración en DevTools).
    - Documentar los problemas detectados con capturas de pantalla y explicaciones.

2. **Pruebas manuales**:
    - Navegar utilizando solo teclado y evaluar:
        - Secuencia lógica de navegación.
        - Visibilidad del foco en elementos interactivos (**WCAG 2.4.11**).
    - Probar componentes interactivos con lectores de pantalla como NVDA o VoiceOver.

3. **Identificación de criterios incumplidos**:
    - Relacionar los problemas encontrados con criterios WCAG 2.2 nivel AA.
    - Priorizar los problemas según su impacto (críticos, moderados, menores).

4. **Entrega de informe inicial**:
    - Documento con:
        - Problemas detectados (pruebas automáticas y manuales).
        - Criterios WCAG 2.2 incumplidos.
        - Prioridad de cada problema.

---

#### **Fase 2: Corrección de problemas**
1. **Implementación de mejoras**:
    - **Semántica HTML**: Corregir etiquetas mal usadas, añadir `alt` a imágenes, y asociar correctamente `label` con campos de formulario.
    - **Estilos y diseño visual**: Ajustar contraste de colores (**1.4.3**), visibilidad del foco (**2.4.11**), y escalabilidad del texto.
    - **Interacción y JavaScript**: Añadir descripciones accesibles (`aria-label`, `aria-describedby`), alternativas a gestos dependientes del ratón (**2.5.7**), y mensajes de error accesibles en formularios (**3.3.1**, **3.3.3**).

2. **Pruebas después de cada mejora**:
    - Repetir pruebas automáticas y manuales para validar las correcciones.

---

#### **Fase 3: Validación final y presentación**
1. **Pruebas finales**:
    - Ejecutar nuevamente las herramientas de testeo y validar con tecnologías asistivas.

2. **Informe final**:
    - Comparativa "antes y después".
    - Explicación de las mejoras aplicadas y su impacto en la accesibilidad.

3. **Presentación del proyecto**:
    - Exposición de los resultados por parte del alumnado.

---

### **Rúbrica de Evaluación**

#### **RA5: Desarrolla interfaces web accesibles**

| **Indicador**                                    | **Excelente (4)**                                                                                              | **Bueno (3)**                                                                                   | **Aceptable (2)**                                                                         | **Insuficiente (1)**                                                      |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| **CE a) Reconoce la necesidad de diseñar webs accesibles** | Explica con profundidad y ejemplos concretos la importancia de la accesibilidad web.                           | Reconoce la importancia de la accesibilidad y menciona pautas clave.                          | Muestra una comprensión básica de la necesidad, pero sin profundizar.                     | No identifica por qué es importante diseñar webs accesibles.              |
| **CE b) Analiza la accesibilidad de documentos web**  | Evalúa con precisión y justifica los problemas detectados en un informe bien estructurado.                     | Detecta problemas de accesibilidad, pero la justificación o documentación es parcial.         | Identifica solo algunos problemas de accesibilidad con una justificación mínima.          | No realiza un análisis correcto ni detecta problemas significativos.      |
| **CE c) Identifica pautas clave de accesibilidad**   | Relaciona pautas específicas de WCAG 2.2 con ejemplos y soluciones aplicables al proyecto.                    | Enumera las pautas clave de WCAG 2.2 y sugiere soluciones generales.                          | Muestra un conocimiento básico de las pautas sin relacionarlas con casos prácticos.       | No identifica pautas o lo hace de forma incorrecta o superficial.         |
| **CE d) Analiza errores según los puntos de verificación** | Identifica errores en profundidad, incluyendo prioridades, impacto y posibles soluciones.                      | Detecta errores y clasifica prioridades, pero sin profundizar en el impacto.                  | Reconoce errores menores o superficiales sin profundizar en las prioridades.              | No analiza errores ni aplica puntos de verificación de WCAG 2.2.          |
| **CE e) Alcanza el nivel de conformidad deseado**   | Cumple con todos los criterios WCAG 2.2 AA, con una implementación técnica impecable y justificada.            | Cumple con la mayoría de los criterios WCAG 2.2 AA, aunque algunos aspectos son mejorables.   | Alcanza el nivel deseado solo parcialmente, dejando varios criterios sin cumplir.          | No alcanza el nivel de conformidad deseado ni implementa mejoras clave.   |
| **CE f) Verifica niveles mediante test externos**   | Realiza pruebas exhaustivas con múltiples herramientas (Lighthouse, Axe, Wave) y documenta claramente resultados. | Usa herramientas externas y documenta parcialmente los resultados.                            | Utiliza herramientas, pero sin suficiente rigor o documentación de los resultados.         | No utiliza herramientas externas o lo hace sin validar adecuadamente.     |
| **CE g) Verifica la visualización en diferentes navegadores y tecnologías** | Realiza pruebas exhaustivas en navegadores (Chrome, Firefox, Edge) y dispositivos, y documenta problemas.       | Realiza pruebas en varios navegadores y tecnologías, aunque omite documentar ciertos casos.   | Verifica la visualización, pero no incluye pruebas en todas las tecnologías requeridas.    | No realiza pruebas suficientes ni valida compatibilidad en navegadores.   |

---

### **Incorporación al proyecto actual**
Este proyecto puede añadirse como un **apartado nuevo** en el material DWEC (UD6) bajo un título como:  
**“Práctica: Análisis y Mejora de Accesibilidad Web según WCAG 2.2”**, integrándolo como una extensión del contenido de interfaces accesibles. Esto refuerza los conocimientos prácticos del alumnado al complementar el material teórico con una aplicación real.

