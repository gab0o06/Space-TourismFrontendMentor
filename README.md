# 🚀 Space Tourism Website - Immersive Frontend Experience

Un sitio web multipágina e interactivo diseñado para simular una plataforma comercial de turismo espacial. Este proyecto fue desarrollado con un enfoque estricto en la fidelidad de diseño (**Pixel Perfect**), animaciones fluidas y una experiencia de usuario (UX) inmersiva, adaptada meticulosamente para dispositivos móviles, tablets y pantallas de escritorio.

🎯 **Demo en Vivo:** [Visita la aplicación desplegada](https://gab0o06.github.io/Space-Tourism/)

---

## 🛠️ Stack Tecnológico

* **Estructura:** HTML5 Semántico
* **Estilos & Layouts:** CSS3 (Flexbox, CSS Grid & Variables Nativas)
* **Interactividad & Estado:** JavaScript Vanilla (ES6+)
* **Workflow:** Diseño Mobile-First & Responsive Adaptable

---

## 🚀 Desafíos Técnicos y Características Clave

* **Arquitectura de UI Basada en Tabs:** En lugar de recargar páginas completas para ver cada planeta, tripulante o tecnología, se desarrolló un sistema dinámico de pestañas (Tabs) mediante manipulación del DOM con JavaScript. Esto reduce la latencia de carga y emula el comportamiento de una SPA (Single Page Application).
* **Manejo Dinámico de Recursos Visuales:** Implementación de fondos de pantalla adaptativos empleando CSS *media queries* avanzados, garantizando que imágenes de alta resolución no ralenticen la carga en dispositivos móviles.
* **Maquetación Compleja:** Combinación de `CSS Grid` para layouts asimétricos (como la sección de tecnología) y `Flexbox` para alineaciones de componentes modulares y barras de navegación.
* **Menú Navegación Mobile:** Menú lateral tipo "hamburguesa" con transiciones suaves y efecto de desenfoque moderno (*backdrop-filter*) para mantener la estética futurista.

---

## 📐 Criterio de Ingeniería y Estructura

Para este desarrollo, el foco principal estuvo en la **mantenibilidad del código** y la **fidelidad del diseño**.

### Componentización y Reutilización en CSS
En lugar de escribir CSS repetitivo, se estructuró el proyecto siguiendo principios de un **Sistema de Diseño (Design System)** utilizando variables CSS globales para tipografías, colores y espaciados (tokens de diseño):

```css
:root {
  /* Color Tokens */
  --clr-dark: 230 35% 7%;
  --clr-light: 231 77% 90%;
  --clr-white: 0 0% 100%;
  
  /* Font Family Tokens */
  --ff-serif: "Bellefair", serif;
  --ff-sans-cond: "Barlow Condensed", sans-serif;
  --ff-sans-normal: "Barlow", sans-serif;
}
```
### Gestión de Estado en JavaScript Vanilla
La interactividad de los paneles (Destination, Crew, Technology) se resolvió centralizando la lógica de intercambio de datos mediante atributos personalizados (`data-* attributes`) en el HTML, permitiendo mutar el contenido del DOM de manera eficiente con un único *Event Listener*:

```javascript
// Enfoque eficiente: Delegación de eventos para optimizar rendimiento
tabList.addEventListener('click', (e) => {
    const targetTab = e.target;
    if (!targetTab.matches('[role="tab"]')) return;
    
    // Lógica optimizada para alternar paneles informativos e imágenes
    switchTab(targetTab);
});
```
### Como ejecutar el proyecto Local
1. Clona el repositorio
```console
git clone [https://github.com/gab0o06/Space-Tourism.git](https://github.com/gab0o06/Space-Tourism.git)
```
3. Abre el archivo index.html
Puedes usar Live Server de VS code para un desarrollo en tiempo real.  
