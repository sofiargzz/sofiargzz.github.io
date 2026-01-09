# plan1.md — Base del portfolio (nivel Vanilla, principiante)

## Prompt (Fase 1)
Quiero un plan simple para hacer una plantilla de portfolio en HTML/CSS/JS (sin frameworks).

Necesito:
- Estructura de carpetas.
- Menú responsive con botón hamburguesa en móvil.
- Tipografía con clamp() y variables CSS.
- Modo oscuro con un botón y guardar la preferencia.
- Scroll suave y marcar el enlace activo según la sección.
- Respetar prefers-reduced-motion.

Dame los pasos en orden, con tareas pequeñas y claras.

---

## Plan (Fase 1 — respuesta de la IA)

### 1) Preparar estructura del proyecto
- Crear archivos:
  - `index.html`
  - `404.html`
  - `assets/css/` → `base.css`, `layout.css`, `components.css`, `index.css`
  - `assets/js/main.js`
  - `docs/plan1.md`

### 2) HTML (estructura semántica)
- En `index.html`:
  - Poner `<header>` con `<nav>`.
  - Añadir un botón de menú para móvil (hamburguesa).
  - Crear enlaces a secciones con ids: `#about`, `#projects`, `#contact`.
  - En `<main>` crear secciones:
    - Hero (con un solo `<h1>`)
    - About
    - Projects
    - Contact
  - Añadir `<footer>` al final.

### 3) CSS (variables + responsive)
- En `base.css`:
  - Definir variables CSS para colores y espacios.
  - Crear tipografía fluida con `clamp()`.
  - Añadir estilos base (body, links, imágenes, focus visible).
- En `layout.css`:
  - Crear `.container` y `.section`.
  - Hacer grids responsive (projects con `auto-fit/minmax`).
- En `components.css`:
  - Estilos del menú (desktop vs móvil).
  - Estilos de botones y tarjetas.
  - Animaciones suaves simples.
- Añadir `@media (prefers-reduced-motion: reduce)` para reducir/evitar animaciones.

### 4) JavaScript (interacciones mínimas)
- Menú móvil:
  - Al clicar el botón hamburguesa: abrir/cerrar el menú.
  - Actualizar `aria-expanded`.
  - Al clicar un enlace: cerrar el menú.
- Modo oscuro:
  - Botón para cambiar tema.
  - Guardar el tema en `localStorage`.
  - Aplicar el tema al cargar la página.
- Enlace activo:
  - Detectar qué sección se ve (con `IntersectionObserver`).
  - Poner clase `.is-active` al enlace correspondiente.

### 5) Comprobaciones rápidas (QA)
- Probar en móvil (320/480), tablet (768) y escritorio (1024+).
- Ver que no hay scroll horizontal.
- Ver que el menú abre/cierra bien.
- Ver que el modo oscuro se guarda al recargar.
- Ver que no hay errores en consola.
- Ver que con prefers-reduced-motion (activado) no haya animaciones molestas.

---

## Notas (Fase 2 — qué implementé)
- Implementé la estructura en `index.html` con secciones y navegación.
- Implementé variables CSS + tipografía con clamp() en `assets/css/base.css`.
- Implementé responsive layout en `assets/css/layout.css` y componentes en `assets/css/components.css`.
- Implementé en `assets/js/main.js`:

