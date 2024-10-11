---
hide:
  - navigation
---

# 4.2 **Guía completa de CSS3**.

---

## Índice

1. [Introducción a CSS3](#introducción-a-css3)
2. [Estructura Básica de CSS](#estructura-básica-de-css)
3. [Selectores CSS](#selectores-css)
    - [Selectores Básicos](#selectores-básicos)
    - [Selectores de Clase y ID](#selectores-de-clase-y-id)
    - [Selectores de Atributo](#selectores-de-atributo)
    - [Selectores de Pseudo-clases y Pseudo-elementos](#selectores-de-pseudo-clases-y-pseudo-elementos)
4. [Modelo de Caja (Box Model)](#modelo-de-caja-box-model)
5. [Propiedades de Texto y Fuente](#propiedades-de-texto-y-fuente)
6. [Colores y Fondos](#colores-y-fondos)
7. [Diseño de Layout](#diseño-de-layout)
    - [Flexbox](#flexbox)
    - [Grid Layout](#grid-layout)
8. [Transiciones y Animaciones](#transiciones-y-animaciones)
9. [Responsividad y Media Queries](#responsividad-y-media-queries)
10. [Nuevas Características de CSS3](#nuevas-características-de-css3)
    - [La Regla `@scope`](#la-regla-scope)
    - [Otras Nuevas Características](#otras-nuevas-características)
11. [Buenas Prácticas en CSS](#buenas-prácticas-en-css)
12. [Uso de CSS3 en React.js](#uso-de-css3-en-reactjs)
13. [Uso de CSS3 en Vue.js](#uso-de-css3-en-vuejs)
14. [Conclusión](#conclusión)

---

## Introducción a CSS3

**CSS3** (Cascading Style Sheets Level 3) es la última versión de CSS, utilizada para describir la presentación de documentos HTML y XML. CSS3 introduce nuevas características y mejoras que facilitan la creación de diseños web más atractivos y funcionales.

### ¿Por qué usar CSS3?

- **Modularidad:** CSS3 se divide en módulos, lo que facilita su uso y comprensión.
- **Nuevas propiedades:** Permite efectos visuales avanzados como sombras, transiciones y animaciones.
- **Responsive Design:** Facilita la creación de sitios web que se adaptan a diferentes tamaños de pantalla.
- **Mejoras en el diseño:** Nuevas herramientas como Flexbox y Grid Layout para layouts más complejos y flexibles.

---

## Estructura Básica de CSS

Un archivo CSS está compuesto por reglas que definen cómo se deben mostrar los elementos HTML.

### Sintaxis Básica

```css
selector {
    propiedad: valor;
}
```

### Ejemplo

```css
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}

h1 {
    color: #333333;
    text-align: center;
}
```

---

## Selectores CSS

Los **selectores** son patrones utilizados para seleccionar los elementos HTML que deseas estilizar.

### Selectores Básicos

- **Selector de Tipo:** Selecciona todos los elementos de un tipo específico.

    ```css
    p {
        color: blue;
    }
    ```

- **Selector Universal:** Selecciona todos los elementos.

    ```css
    * {
        margin: 0;
        padding: 0;
    }
    ```

### Selectores de Clase y ID

- **Clase:** Selecciona elementos con una clase específica.

    ```css
    .mi-clase {
        background-color: yellow;
    }
    ```

- **ID:** Selecciona un elemento con un ID específico (debe ser único).

    ```css
    **#**mi-id {
        border: 1px solid black;
    }
    ```

### Selectores de Atributo

Seleccionan elementos basados en atributos o valores de atributos.

```css
input[type="text"] {
    width: 200px;
    padding: 5px;
}
```
### Selectores de Pseudo-clases y Pseudo-elementos

- **Pseudo-clases:** Seleccionan elementos en un estado específico.

    ```css
    a:hover {
        color: red;
    }
    ```

- **Pseudo-elementos:** Seleccionan una parte específica de un elemento.

    ```css
    p::first-line {
        font-weight: bold;
    }
    ```
---

## Modelo de Caja (Box Model)

El **Box Model** de CSS describe cómo se calculan las dimensiones y el espacio alrededor de los elementos.

### Componentes del Box Model

1. **Contenido:** Área donde se muestra el contenido (texto, imágenes, etc.).
2. **Padding (Relleno):** Espacio entre el contenido y el borde.
3. **Border (Borde):** Línea que rodea el padding y el contenido.
4. **Margin (Margen):** Espacio fuera del borde.

### Ejemplo

```css
div {
    width: 300px;
    padding: 20px;
    border: 5px solid #333;
    margin: 15px;
}
```

### Visualización

```
+-----------------------------+
|          Margin             |
|  +-----------------------+  |
|  |        Border         |  |
|  |  +-----------------+  |  |
|  |  |     Padding     |  |  |
|  |  |  +-----------+  |  |  |
|  |  |  |  Content  |  |  |  |
|  |  |  +-----------+  |  |  |
|  |  +-----------------+  |  |
|  +-----------------------+  |
+-----------------------------+
```

---

## Propiedades de Texto y Fuente

CSS3 ofrece una amplia gama de propiedades para estilizar el texto.

### Tipografía

- **font-family:** Define la familia de fuentes.

    ```css
    body {
        font-family: 'Helvetica Neue', sans-serif;
    }
    ```

- **font-size:** Tamaño de la fuente.

     ```css
    h1 {
        font-size: 2em;
    }
    ```

- **font-weight:** Grosor de la fuente.

     ```css
    p {
        font-weight: bold;
    }
    ```

- **font-style:** Estilo de la fuente (normal, italic, oblique).

    ```css
    em {
        font-style: italic;
    }
    ```

### Propiedades de Texto

- **color:** Color del texto.

     ```css
    span {
        color: #ff5733;
    }
    ```

- **text-align:** Alineación del texto.

    ```css
    .centrado {
        text-align: center;
    }
    ```

- **text-decoration:** Decoraciones del texto (subrayado, tachado, etc.).

    ```css
    a {
        text-decoration: none;
    }
    a:hover {
        text-decoration: underline;
    }
    ```

- **line-height:** Altura de la línea.

    ```css
    p {
        line-height: 1.6;
    }
    ```

---

## Colores y Fondos

### Colores

Puedes definir colores usando nombres, códigos hexadecimales, RGB, RGBA, HSL y HSLA.

```css
h2 {
    color: #3498db; /* Hexadecimal */
}

p {
    color: rgb(52, 152, 219); /* RGB */
}

div {
    background-color: rgba(52, 152, 219, 0.5); /* RGBA */
}
```

### Fondos

- **background-color:** Color de fondo.
- **background-image:** Imagen de fondo.
- **background-repeat:** Repetición de la imagen.
- **background-size:** Tamaño de la imagen de fondo.
- **background-position:** Posición de la imagen de fondo.


```css
body {
    background-color: #ecf0f1;
    background-image: url('fondo.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
```

---

## Diseño de Layout

### Flexbox

**Flexbox** es un modelo de diseño unidimensional que facilita la alineación y distribución de elementos dentro de un contenedor.

#### Contenedor Flex

```css
.container {
    display: flex;
    flex-direction: row; /* column, row-reverse, column-reverse */
    justify-content: space-between; /* flex-start, flex-end, center, space-around, space-evenly */
    align-items: center; /* stretch, flex-start, flex-end, center, baseline */
}
```

#### Elementos Flex

```css
.item {
    flex: 1; /* grow, shrink, basis */
    margin: 10px;
}
```

#### Ejemplo Completo

```html
<div class="container">
    <div class="item">Elemento 1</div>
    <div class="item">Elemento 2</div>
    <div class="item">Elemento 3</div>
</div>
```

```css
.container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 200px;
    background-color: #f8f9fa;
}

.item {
    background-color: #007bff;
    color: white;
    padding: 20px;
    border-radius: 5px;
}
```

### Grid Layout

**Grid Layout** es un sistema de diseño bidimensional que permite crear estructuras complejas con filas y columnas.

#### Contenedor Grid

```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 columnas de igual tamaño */
    grid-gap: 10px; /* Espacio entre filas y columnas */
}
```

#### Elementos Grid

```css
.grid-item {
    background-color: #28a745;
    color: white;
    padding: 20px;
    text-align: center;
}
```

#### Ejemplo Completo

```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
    <div class="grid-item">4</div>
    <div class="grid-item">5</div>
    <div class="grid-item">6</div>
</div>
```

```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 15px;
    background-color: #f1f1f1;
    padding: 10px;
}

.grid-item {
    background-color: #28a745;
    color: white;
    padding: 30px 0;
    font-size: 30px;
    text-align: center;
}
```

---

## Transiciones y Animaciones

### Transiciones

Las **transiciones** permiten cambiar las propiedades CSS de un elemento de manera suave durante un período de tiempo.

#### Sintaxis

```css
.selector {
    transition: propiedad duración timing-función retraso;
}
```

#### Ejemplo

```css
button {
    background-color: #3498db;
    color: white;
    padding: 10px 20px;
    border: none;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #2980b9;
}
```

### Animaciones

Las **animaciones** permiten definir una serie de estilos que cambian a lo largo del tiempo.

#### Sintaxis

```css
@keyframes nombre-animación {
    desde { /* estilos iniciales */ }
    hasta { /* estilos finales */ }
}

.selector {
    animation: nombre-animación duración timing-función retraso iteraciones dirección relleno;
}
```

#### Ejemplo

```css
@keyframes girar {
    from {
        transform: rotate(0deg);
    }
    to {
        transform: rotate(360deg);
    }
}

.icono {
    display: inline-block;
    animation: girar 2s linear infinite;
}
```

```html
<div class="icono">🔄</div>
```

---

## Responsividad y Media Queries

Las **Media Queries** permiten aplicar estilos CSS específicos según las características del dispositivo, como el ancho de la pantalla.

### Ejemplo Básico

```css
/* Estilos por defecto */
body {
    font-size: 16px;
}

/* Para pantallas con un ancho máximo de 768px */
@media (max-width: 768px) {
    body {
        font-size: 14px;
    }
}

/* Para pantallas con un ancho máximo de 480px */
@media (max-width: 480px) {
    body {
        font-size: 12px;
    }
}
```

### Diseño Responsive con Flexbox

```css
.container {
    display: flex;
    flex-wrap: wrap;
}

.item {
    flex: 1 1 300px; /* grow, shrink, basis */
    margin: 10px;
}

/* Ajuste para pantallas pequeñas */
@media (max-width: 600px) {
    .container {
        flex-direction: column;
    }
}
```

---

## Nuevas Características de CSS3

### La Regla `@scope`

La regla `@scope` es una **propuesta avanzada** en CSS que permite definir un ámbito específico dentro del cual se aplican ciertas reglas de estilo. Esto facilita el encapsulamiento de estilos, evitando conflictos globales y mejorando la mantenibilidad del código CSS.

#### Sintaxis Básica

```css
@scope .mi-contenedor {
    /* Reglas CSS aquí solo aplicarán dentro de .mi-contenedor */
    h1 {
        color: blue;
    }

    .boton {
        background-color: green;
    }
}
```

#### Estado Actual de la Regla `@scope`

Hasta la fecha de mi conocimiento (octubre de 2023), la regla `@scope` aún está en etapa de propuesta y **no es soportada de manera nativa** por la mayoría de los navegadores. Por lo tanto, su uso directo en proyectos web estándar **no es factible**. Sin embargo, entender su funcionamiento es beneficioso para futuros desarrollos y para aprovechar otras técnicas de encapsulamiento de estilos disponibles en frameworks modernos como React y Vue.

#### Ejemplo (Propuesta)

```css
@scope .mi-contenedor {
    h1 {
        color: blue;
    }

    .boton {
        background-color: green;
    }
}
```

En este ejemplo, las reglas dentro de `@scope .mi-contenedor` solo se aplicarán a los elementos que estén dentro del contenedor con la clase `mi-contenedor`.

### Otras Nuevas Características

Además de la regla `@scope`, CSS3 ha introducido múltiples nuevas características que mejoran la capacidad de diseño y estilización de las páginas web:

- **Variables CSS (`--variable`):** Permiten definir variables reutilizables para colores, tamaños, etc.

    ```css
    :root {
        --color-primario: #3498db;
        --padding-base: 10px;
    }

    .boton {
        background-color: var(--color-primario);
        padding: var(--padding-base);
    }
    ```

- **Propiedades de Sombra (`box-shadow`, `text-shadow`):** Para agregar sombras a elementos y textos.

    ```css
    .caja {
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    h1 {
        text-shadow: 2px 2px #ff0000;
    }
    ```

- **Transformaciones 2D y 3D (`transform`):** Para rotaciones, escalados, traslaciones y más.

    ```css
    .elemento {
        transform: rotate(45deg) scale(1.2);
    }
    ```

- **Filtros CSS (`filter`):** Para aplicar efectos visuales como desenfoques y cambios de color.

    ```css
    img {
        filter: grayscale(50%);
    }
    ```

- **Clipping y Masking (`clip-path`, `mask`):** Para crear formas complejas y máscaras en elementos.

    ```css
    .caja {
        clip-path: circle(50%);
    }
    ```

---

## Buenas Prácticas en CSS

1. **Organización del Código:**
    - Utiliza comentarios para separar secciones.
    - Agrupa selectores relacionados.
    - Sigue una estructura lógica (por ejemplo, de lo general a lo específico).

2. **Nomenclatura Consistente:**
    - Sigue convenciones como **BEM** (Block Element Modifier) para nombrar clases.

    ```css
    /* BEM Example */
    .tarjeta {
        /* Block */
    }

    .tarjeta__titulo {
        /* Element */
    }

    .tarjeta__titulo--destacado {
        /* Modifier */
    }
    ```

3. **Evita el Uso Excesivo de `!important`:**
    - Solo úsalo cuando sea absolutamente necesario para sobreescribir estilos específicos.

4. **Optimización de Selectores:**
    - Utiliza selectores específicos para mejorar el rendimiento.
    - Evita selectores demasiado generales que puedan afectar a muchos elementos innecesariamente.

5. **Uso de Variables CSS:**
    - Define variables para colores, tamaños y otros valores repetitivos.

    ```css
    :root {
        --color-primario: #3498db;
        --padding-base: 10px;
    }

    .boton {
        background-color: var(--color-primario);
        padding: var(--padding-base);
    }
    ```

6. **Compatibilidad entre Navegadores:**
    - Utiliza prefijos de proveedores cuando sea necesario para asegurar la compatibilidad.

    ```css
    .caja {
        -webkit-border-radius: 10px;
        -moz-border-radius: 10px;
        border-radius: 10px;
    }
    ```

7. **Minimización y Compresión:**
    - Minimiza los archivos CSS para reducir el tamaño y mejorar la carga.
    - Utiliza herramientas de compresión como **CSSNano** o **UglifyCSS**.

8. **Evita el CSS Innecesario:**
    - Remueve estilos no utilizados para mantener el código limpio y eficiente.

---

## Uso de CSS3 en React.js

**React.js** es una biblioteca de JavaScript para construir interfaces de usuario. Integrar CSS3 en React permite estilizar componentes de manera eficiente y modular. A continuación, se presentan varias formas de utilizar CSS3 en aplicaciones React.

### 1. Archivos CSS Tradicionales

La forma más sencilla de aplicar CSS en React es mediante la importación de archivos CSS tradicionales.

#### Ejemplo

```jsx
// App.js
import React from 'react';
import './App.css';

function App() {
    return (
        <div className="app-container">
            <h1 className="app-title">¡Hola, React!</h1>
            <button className="app-button">Haz Clic</button>
        </div>
    );
}

export default App;
```

```css
/* App.css */
.app-container {
    text-align: center;
    padding: 50px;
    background-color: #f0f0f0;
}

.app-title {
    color: #3498db;
    font-size: 2.5em;
}

.app-button {
    background-color: #2ecc71;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.app-button:hover {
    background-color: #27ae60;
}
```

### 2. CSS Modules

**CSS Modules** permiten escribir CSS de manera modular y evitar conflictos de nombres de clases mediante el uso de nombres únicos generados automáticamente.

#### Configuración

Si utilizas **Create React App**, los CSS Modules están soportados de forma predeterminada. Simplemente, nombra tus archivos CSS con la extensión `.module.css`.

#### Ejemplo

```css
/* Button.module.css */
.boton {
    background-color: #e74c3c;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    transition: transform 0.2s ease;
}

.boton:hover {
    transform: scale(1.05);
}
```

```jsx
// Button.js
import React from 'react';
import styles from './Button.module.css';

function Button({ children }) {
    return <button className={styles.boton}>{children}</button>;
}

export default Button;
```

### 3. Estilos en Línea (Inline Styles)

Los estilos en línea permiten aplicar estilos directamente en los elementos mediante objetos de JavaScript. Son útiles para estilos dinámicos.

#### Ejemplo

```jsx
// InlineStyleComponent.js
import React from 'react';

function InlineStyleComponent() {
    const estilo = {
        backgroundColor: '#9b59b6',
        color: 'white',
        padding: '15px 30px',
        border: 'none',
        borderRadius: '5px',
        cursor: 'pointer',
        fontSize: '1em',
    };

    return <button style={estilo}>Estilo en Línea</button>;
}

export default InlineStyleComponent;
```

### 4. Styled-Components

**Styled-Components** es una biblioteca que permite escribir CSS en JavaScript, proporcionando estilos encapsulados y dinámicos.

#### Instalación

```bash
npm install styled-components
```

#### Ejemplo

```jsx
// StyledButton.js
import React from 'react';
import styled from 'styled-components';

const Boton = styled.button`
    background-color: #f39c12;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;

    &:hover {
        background-color: #d35400;
    }
`;

function StyledButton({ children }) {
    return <Boton>{children}</Boton>;
}

export default StyledButton;
```

### 5. Ejemplo Completo

```jsx
// App.js
import React from 'react';
import './App.css';
import Button from './Button';
import InlineStyleComponent from './InlineStyleComponent';
import StyledButton from './StyledButton';

function App() {
    return (
        <div className="app-container">
            <h1 className="app-title">Integrando CSS en React</h1>
            <Button>CSS Module Button</Button>
            <InlineStyleComponent />
            <StyledButton>Styled Components Button</StyledButton>
        </div>
    );
}

export default App;
```

```css
/* App.css */
.app-container {
    text-align: center;
    padding: 50px;
    background-color: #f0f0f0;
}

.app-title {
    color: #3498db;
    font-size: 2.5em;
    margin-bottom: 30px;
}
```

---

## Uso de CSS3 en Vue.js

**Vue.js** es un framework progresivo de JavaScript para construir interfaces de usuario. Vue facilita la integración de CSS3 mediante varias metodologías que promueven la modularidad y el alcance de los estilos.

### 1. Estilos Globales

Al igual que en React, puedes utilizar archivos CSS globales que se aplican a toda la aplicación.

#### Ejemplo

```html
<!-- App.vue -->
<template>
  <div id="app">
    <h1 class="app-title">¡Hola, Vue!</h1>
    <button class="app-button">Haz Clic</button>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style src="./App.css"></style>
```

```css
/* App.css */
#app {
    text-align: center;
    padding: 50px;
    background-color: #f0f0f0;
}

.app-title {
    color: #8e44ad;
    font-size: 2.5em;
}

.app-button {
    background-color: #16a085;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.app-button:hover {
    background-color: #148f77;
}
```

### 2. Estilos Escopados (Scoped Styles)

Vue permite encapsular los estilos dentro de componentes mediante el atributo `scoped`. Esto asegura que los estilos definidos solo afecten al componente en el que están definidos.

#### Ejemplo

```html
<!-- Boton.vue -->
<template>
  <button class="boton">Botón Scoped</button>
</template>

<script>
export default {
  name: 'Boton',
};
</script>

<style scoped>
.boton {
    background-color: #e67e22;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;
}

.boton:hover {
    background-color: #d35400;
}
</style>
```

```html
<!-- App.vue -->
<template>
  <div id="app">
    <h1 class="app-title">Integrando CSS en Vue</h1>
    <Boton />
  </div>
</template>

<script>
import Boton from './components/Boton.vue';

export default {
  name: 'App',
  components: {
    Boton,
  },
};
</script>

<style>
/* Estilos Globales */
.app-title {
    color: #8e44ad;
    font-size: 2.5em;
    margin-bottom: 30px;
}
</style>
```

### 3. CSS Modules

Vue también soporta **CSS Modules** para una mayor modularidad y evitar conflictos de nombres.

#### Configuración

Si utilizas **Vue CLI**, puedes habilitar CSS Modules añadiendo `module` en la etiqueta `<style>`.

#### Ejemplo

```html
<!-- Tarjeta.vue -->
<template>
  <div :class="$style.tarjeta">
    <h2 :class="$style.titulo">Título de la Tarjeta</h2>
    <p :class="$style.descripcion">Descripción de la tarjeta.</p>
    <button :class="$style.boton">Acción</button>
  </div>
</template>

<script>
export default {
  name: 'Tarjeta',
};
</script>

<style module>
.tarjeta {
    background-color: #2c3e50;
    color: white;
    padding: 20px;
    border-radius: 8px;
    text-align: center;
    margin: 20px 0;
}

.titulo {
    font-size: 1.5em;
    margin-bottom: 10px;
}

.descripcion {
    font-size: 1em;
    margin-bottom: 20px;
}

.boton {
    background-color: #e74c3c;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.boton:hover {
    background-color: #c0392b;
}
</style>
```

### 4. Styled-Components en Vue.js

Aunque **Styled-Components** es más común en React, también se puede utilizar en Vue mediante bibliotecas adicionales como [vue-styled-components](https://github.com/styled-components/vue-styled-components).

#### Instalación

```bash
npm install vue-styled-components
```

#### Ejemplo

```html
<!-- StyledButton.vue -->
<template>
  <BotonComponent>
    {{ children }}
  </BotonComponent>
</template>

<script>
import styled from 'vue-styled-components';

const BotonComponent = styled.button`
    background-color: #e67e22;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;

    &:hover {
        background-color: #d35400;
    }
`;

export default {
  name: 'StyledButton',
  components: {
    BotonComponent,
  },
  props: {
    children: {
      type: String,
      required: true,
    },
  },
};
</script>
```

### 5. Ejemplo Completo

```html
<!-- App.vue -->
<template>
  <div id="app">
    <h1 class="app-title">Integrando CSS en Vue</h1>
    <Boton />
    <Tarjeta />
    <Alerta tipo="success">¡Operación Exitosa!</Alerta>
    <Alerta tipo="error">¡Ha ocurrido un error!</Alerta>
  </div>
</template>

<script>
import Boton from './components/Boton.vue';
import Tarjeta from './components/Tarjeta.vue';
import Alerta from './components/Alerta.vue';

export default {
  name: 'App',
  components: {
    Boton,
    Tarjeta,
    Alerta,
  },
};
</script>

<style>
/* Estilos Globales */
.app-title {
    color: #8e44ad;
    font-size: 2.5em;
    margin-bottom: 30px;
}
</style>
```

```html
<!-- Alerta.vue -->
<template>
  <div :class="['alerta', tipo]">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Alerta',
  props: {
    tipo: {
      type: String,
      default: 'info', // 'success', 'error', 'warning'
    },
  },
};
</script>

<style scoped>
.alerta {
    padding: 15px;
    border-radius: 5px;
    margin: 10px 0;
    color: white;
}

.success {
    background-color: #27ae60;
}

.error {
    background-color: #c0392b;
}

.warning {
    background-color: #f39c12;
}

.info {
    background-color: #2980b9;
}
</style>
```

---

## Mejores Opciones para React.js y Vue.js

### Mejor Opción para React.js

Para la mayoría de los proyectos en **React**, las opciones más recomendadas son **CSS Modules** y **Styled-Components** debido a su capacidad para encapsular estilos, evitar conflictos y mejorar la mantenibilidad.

#### 1. CSS Modules

**Descripción:**
CSS Modules permiten escribir CSS de manera modular y evitar conflictos de nombres de clases mediante el uso de nombres únicos generados automáticamente.

**Ventajas:**
- **Encapsulamiento de Estilos:** Evita colisiones de nombres de clases.
- **Mantenibilidad:** Facilita la gestión de estilos en proyectos grandes.
- **Compatibilidad:** Soportado de forma nativa por herramientas como Create React App.

**Desventajas:**
- **Curva de Aprendizaje:** Requiere familiarizarse con la sintaxis específica.
- **Limitaciones Dinámicas:** Menos flexible para estilos altamente dinámicos en comparación con CSS-in-JS.

**Ejemplo:**

```css
/* Boton.module.css */
.boton {
    background-color: #e67e22;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;
}

.boton:hover {
    background-color: #d35400;
}
```

```jsx
// Boton.jsx
import React from 'react';
import styles from './Boton.module.css';

function Boton({ children }) {
    return <button className={styles.boton}>{children}</button>;
}

export default Boton;
```

#### 2. Styled-Components (CSS-in-JS)

**Descripción:**
Styled-Components es una biblioteca que permite escribir CSS directamente en archivos JavaScript, proporcionando estilos encapsulados y dinámicos.

**Ventajas:**
- **Scoped Styles:** Los estilos están vinculados directamente a los componentes.
- **Dinamicidad:** Facilita la aplicación de estilos basados en props o estados.
- **Mantenimiento:** Mejora la mantenibilidad al mantener estilos y lógica juntos.

**Desventajas:**
- **Performance:** Puede introducir una sobrecarga de rendimiento en aplicaciones muy grandes.
- **Dependencia de Librería Externa:** Añade una dependencia adicional al proyecto.

**Ejemplo:**

```jsx
// StyledButton.jsx
import React from 'react';
import styled from 'styled-components';

const Boton = styled.button`
    background-color: #f39c12;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;

    &:hover {
        background-color: #d35400;
    }
`;

function StyledButton({ children }) {
    return <Boton>{children}</Boton>;
}

export default StyledButton;
```

### Mejor Opción para Vue.js

Para **Vue.js**, las opciones más recomendadas son **Estilos Escopados (`scoped`)** y **CSS Modules**.

#### 1. Estilos Escopados (`scoped`)

**Descripción:**
Vue permite encapsular los estilos dentro de componentes mediante el atributo `scoped` en la etiqueta `<style>`. Esto asegura que los estilos definidos solo afecten al componente actual.

**Ventajas:**
- **Encapsulamiento Automático:** No requiere configuración adicional.
- **Simplicidad:** Fácil de implementar y entender.
- **Compatibilidad:** Funciona de manera nativa con Vue Single File Components (SFC).

**Desventajas:**
- **Limitaciones en Selectores Globales:** No es adecuado para estilos que deben aplicarse globalmente.
- **Reutilización:** Menos eficiente para estilos reutilizables en múltiples componentes.

**Ejemplo:**

```html
<!-- Boton.vue -->
<template>
  <button class="boton">Botón Scoped</button>
</template>

<script>
export default {
  name: 'Boton',
};
</script>

<style scoped>
.boton {
    background-color: #e67e22;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease;
}

.boton:hover {
    background-color: #d35400;
}
</style>
```

#### 2. CSS Modules

**Descripción:**
Al igual que en React, Vue soporta **CSS Modules** para una mayor modularidad y evitar conflictos de nombres.

**Ventajas:**
- **Encapsulamiento de Estilos:** Evita colisiones de nombres de clases.
- **Reutilización:** Facilita la reutilización de estilos en múltiples componentes.
- **Integración con Herramientas Modernas:** Funciona bien con Vue CLI y otras herramientas de construcción.

**Desventajas:**
- **Configuración Adicional:** Requiere una configuración específica en algunos casos.
- **Sintaxis:** Puede ser menos intuitivo para quienes están acostumbrados a CSS tradicional.

**Ejemplo:**

```html
<!-- Tarjeta.vue -->
<template>
  <div :class="$style.tarjeta">
    <h2 :class="$style.titulo">Título de la Tarjeta</h2>
    <p :class="$style.descripcion">Descripción de la tarjeta.</p>
    <button :class="$style.boton">Acción</button>
  </div>
</template>

<script>
export default {
  name: 'Tarjeta',
};
</script>

<style module>
.tarjeta {
    background-color: #2c3e50;
    color: white;
    padding: 20px;
    border-radius: 8px;
    text-align: center;
    margin: 20px 0;
}

.titulo {
    font-size: 1.5em;
    margin-bottom: 10px;
}

.descripcion {
    font-size: 1em;
    margin-bottom: 20px;
}

.boton {
    background-color: #e74c3c;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.boton:hover {
    background-color: #c0392b;
}
</style>
```

---

## Conclusión

### Para React.js:

- **CSS Modules** y **Styled-Components** son las opciones más recomendadas.
    - **CSS Modules** son ideales para mantener CSS separado y modular.
    - **Styled-Components** son excelentes para estilos dinámicos y encapsulados directamente en los componentes.

### Para Vue.js:

- **Estilos Escopados (`scoped`)** son la opción predeterminada y más sencilla para encapsular estilos dentro de componentes individuales.
- **CSS Modules** son recomendables para proyectos que requieren una mayor modularidad y reutilización de estilos.

### Sobre la Regla `@scope`:

Aunque la regla `@scope` de CSS3 ofrece una forma prometedora de encapsular estilos directamente en CSS, **su falta de soporte amplio** en navegadores la hace **impráctica** para su uso inmediato en proyectos de React y Vue. En su lugar, aprovechar las herramientas y métodos proporcionados por estos frameworks garantiza un encapsulamiento efectivo y mantenible de los estilos.

### Recomendaciones Generales:

- Mantén una **nomenclatura consistente** para clases y selectores.
- **Organiza** los estilos de manera lógica y modular.
- **Sigue las mejores prácticas** para asegurar la escalabilidad y mantenibilidad de tu código CSS.
- **Utiliza herramientas de preprocesamiento** como **Sass** o **Less** si tu proyecto lo requiere.
- **Optimiza el rendimiento** minimizando y compresionando los archivos CSS.

---
