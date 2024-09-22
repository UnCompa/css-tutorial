# Temario de CSS

## Nivel 1: Fundamentos de CSS

### Sección 1: Introducción a CSS

- **Tema 1: ¿Qué es CSS?**
  - Concepto: Hojas de estilo en cascada para diseñar y dar formato a documentos HTML.
  - Historia y evolución de CSS.
  - Ejemplo básico:

    ```html
    <style>
      h1 {
        color: blue;
        font-size: 24px;
      }
    </style>
    ```

- **Tema 2: Sintaxis básica de CSS**
  - Selectores: Cómo seleccionar elementos HTML para aplicar estilos.
  - Propiedades y valores CSS.
  - Ejemplo:

    ```css
    p {
      color: red;
      font-size: 18px;
    }
    ```

### Sección 2: Selectores CSS

- **Tema 1: Selectores básicos**
  - Tipos de selectores: por elemento, clase (`.clase`), ID (`#id`), universal (`*`).
  - Ejemplo:

    ```css
    h1 { color: green; }
    .miClase { background-color: yellow; }
    #miID { font-weight: bold; }
    ```

- **Tema 2: Selectores avanzados**
  - Selectores descendientes, hijos directos, adyacentes, de atributo.
  - Ejemplo:

    ```css
    div > p { color: blue; }
    input[type="text"] { border: 1px solid gray; }
    ```

### Sección 3: Propiedades fundamentales de CSS

- **Tema 1: Color y fondo**
  - Propiedad `color` para texto y `background-color` para fondo.
  - Fondos con imágenes (`background-image`).
  - Ejemplo:

    ```css
    body { background-color: lightgray; }
    ```

- **Tema 2: Tipografía**
  - Propiedades `font-family`, `font-size`, `font-weight`, `line-height`.
  - Uso de fuentes web y Google Fonts.
  - Ejemplo:

    ```css
    p {
      font-family: Arial, sans-serif;
      font-size: 16px;
    }
    ```

### Sección 4: Modelo de caja (Box Model)

- **Tema 1: Margen, relleno y borde**
  - Propiedades `margin`, `padding` y `border`.
  - Cómo afecta el espacio alrededor de los elementos.
  - Ejemplo:

    ```css
    div {
      margin: 10px;
      padding: 20px;
      border: 1px solid black;
    }
    ```

- **Tema 2: Tamaño de los elementos**
  - Propiedades `width`, `height`, y cómo funcionan con el modelo de caja.
  - Ejemplo:

    ```css
    img {
      width: 100px;
      height: auto;
    }
    ```

---

## Nivel 2: Intermedio

### Sección 1: Layouts y diseño

- **Tema 1: Display y posicionamiento**
  - Propiedades `display` (`block`, `inline`, `inline-block`, `none`).
  - Propiedad `position`: `static`, `relative`, `absolute`, `fixed`.
  - Ejemplo:

    ```css
    .box {
      display: inline-block;
      position: relative;
      top: 10px;
    }
    ```

- **Tema 2: Flexbox**
  - Estructura de diseño flexible.
  - Propiedades como `flex-direction`, `justify-content`, `align-items`, `flex-wrap`.
  - Ejemplo:

    ```css
    .container {
      display: flex;
      justify-content: center;
    }
    ```

- **Tema 3: Grid Layout**
  - Diseño en dos dimensiones con CSS Grid.
  - Propiedades como `grid-template-columns`, `grid-template-rows`, `grid-gap`.
  - Ejemplo:

    ```css
    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
    }
    ```

### Sección 2: Pseudoclases y Pseudoelementos

- **Tema 1: Pseudoclases**
  - Selectores dinámicos con pseudoclases: `:hover`, `:focus`, `:nth-child()`, `:nth-of-type()`.
  - Ejemplo:

    ```css
    a:hover {
      color: red;
    }
    ```

- **Tema 2: Pseudoelementos**
  - Selección de partes específicas de un elemento: `::before`, `::after`, `::first-letter`, `::first-line`.
  - Ejemplo:

    ```css
    p::first-letter {
      font-size: 2em;
      color: blue;
    }
    ```

### Sección 3: Efectos y animaciones

- **Tema 1: Transiciones**
  - Transiciones suaves entre estados de los elementos.
  - Propiedades como `transition`, `transition-duration`, `transition-timing-function`.
  - Ejemplo:

    ```css
    button {
      background-color: blue;
      transition: background-color 0.5s ease;
    }
    button:hover {
      background-color: red;
    }
    ```

- **Tema 2: Transformaciones**
  - Propiedades `transform`, `scale`, `rotate`, `translate`.
  - Ejemplo:

    ```css
    .box {
      transform: rotate(45deg);
    }
    ```

- **Tema 3: Animaciones**
  - Uso de `@keyframes` para crear animaciones.
  - Propiedades `animation`, `animation-duration`, `animation-iteration-count`.
  - Ejemplo:

    ```css
    @keyframes girar {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    .animado {
      animation: girar 2s infinite;
    }
    ```

---

## Nivel 3: Avanzado

### Sección 1: Responsive Design

- **Tema 1: Media Queries**
  - Uso de `@media` para aplicar estilos según el tamaño de la pantalla.
  - Ejemplo:

    ```css
    @media (max-width: 600px) {
      body {
        background-color: lightblue;
      }
    }
    ```

- **Tema 2: Diseño móvil primero (Mobile First)**
  - Diseño pensando en dispositivos móviles antes que en pantallas grandes.
  - Ejemplo:

    ```css
    body {
      font-size: 16px;
    }
    @media (min-width: 768px) {
      body {
        font-size: 18px;
      }
    }
    ```

### Sección 2: Preprocesadores CSS (Sass)

- **Tema 1: Variables en CSS**
  - Uso de variables CSS para facilitar el mantenimiento de los estilos.
  - Ejemplo:

    ```css
    :root {
      --main-color: #3498db;
    }
    body {
      color: var(--main-color);
    }
    ```

- **Tema 2: Introducción a Sass**
  - Concepto de preprocesadores: funciones avanzadas con CSS.
  - Uso de variables, anidación, mixins.
  - Ejemplo:

    ```scss
    $color-principal: #3498db;

    body {
      background-color: $color-principal;
    }
    ```

### Sección 3: Buenas prácticas y optimización

- **Tema 1: Escribir CSS modular**
  - Cómo organizar los estilos CSS para un código más legible y mantenible.
  - BEM (Block, Element, Modifier) como metodología de organización de clases.

- **Tema 2: Optimización de rendimiento**
  - Minimizar y agrupar archivos CSS.
  - Uso de herramientas como `Autoprefixer` y `CSS Minify`.

---

## Nivel 4: Temas Avanzados

### Sección 1: CSS Variables (Custom Properties)

- **Tema 1: Definir y usar variables**
  - Declaración de variables en CSS y su uso en diferentes partes del proyecto.
  - Ejemplo:

    ```css
    :root {
      --main-bg-color: #333;
      --main-text-color: #fff;
    }

    body {
      background-color: var(--main-bg-color);
      color: var(--main-text-color);
    }
    ```

- **Tema 2: Variables dinámicas**
  - Cambiar valores de variables con JavaScript o mediante pseudoclases.
  - Ejemplo:

    ```css
    body.dark-mode {
      --main-bg-color: #000;
      --main-text-color: #fff;
    }
    ```

### Sección 2: CSS Grid y Flexbox combinados

- **Tema 1: Combinación de Flexbox y Grid**
  - Aplicar Flexbox y Grid juntos para crear layouts complejos y adaptables.
  - Ejemplo:

    ```css
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
    }

    .item {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    ```

### Sección 3: Técnicas avanzadas de diseño responsivo

- **Tema 1: Un

idades CSS avanzadas**

- Uso de unidades relativas como `vw`, `vh`, `vmin`, `vmax`, y unidades absolutas como `rem`, `em`.
- Ejemplo:

    ```css
    .hero {
      height: 100vh;
    }
    ```

- **Tema 2: Uso avanzado de media queries**
  - Aplicación de media queries avanzadas, incluyendo características como orientación de la pantalla, resolución, etc.
  - Ejemplo:

    ```css
    @media (orientation: landscape) {
      .container {
        flex-direction: row;
      }
    }
    ```
