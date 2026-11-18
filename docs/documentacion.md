# Documentación Técnica del Portfolio — Braian Nahuel Basualdo

**Curso:** 6.º Año · Informática  
**Institución:** Instituto Privado Mixto San Agustín (Córdoba, Argentina)  
**Versión:** 1.0 (Sitio estático para GitHub Pages)

---

## 1. Propósito del Proyecto

Este portfolio web presenta de forma ordenada el perfil técnico, académico y práctico de **Braian Nahuel Basualdo**. Fue desarrollado íntegramente con **HTML5 semántico**, **CSS3 moderno** y **JavaScript nativo**, sin frameworks ni dependencias externas, para desplegarse directamente en **GitHub Pages**.

### Contenido integrado
- **Presentación con ficha técnica lateral (sin foto):** Monograma `BB`, edad (18 años), formación, áreas de enfoque y disponibilidad horaria.
- **Sobre mí (Bento Grid):** Perfil personal, objetivo laboral, experiencia en armado/mantenimiento de PC y notebooks, entrenamiento físico (1 a 3 años, preparación y seguimiento de rutinas) y horarios/idiomas.
- **Proyectos (con filtros y modal):**
  1. Autitos seguidores de línea
  2. Desarrollo de páginas web (HTML y CSS)
  3. Robots básicos y prototipos educativos
  4. Diseño de aplicación empresarial — Tech Camp UCC
- **Competencias y logros:** Copa Robótica 2026 (Semifinales), Iron Bot Córdoba, Tech Camp 2026 (UCC) y Cuadro de Honor desde 1.º año.
- **Habilidades y Contacto:** Conocimientos informáticos, competencias personales, correo (`brabasualdo4@gmail.com`) y teléfono (`3517310050`) con botones de copiado.

---

## 2. Sistema Visual: Azul Profundo y Cobalto con Amarillo Tenue

| Token CSS | Valor | Función |
| :--- | :--- | :--- |
| `--blue-950` | `#0b192c` | Ficha técnica lateral, encabezados y contraste oscuro |
| `--blue-900` | `#132a4a` | Azul marino base de marca y degradados |
| `--blue-700` | `#1d4ed8` | Acentos principales, enlaces y bordes activos |
| `--blue-50` | `#eff6ff` | Fondos suaves de lectura y tarjetas secundarias |
| `--yellow-100` | `#fef9c3` | Amarillo tenue para badges, botones suaves y resaltados |
| `--yellow-200` | `#fef08a` | Bordes suaves y hover en amarillo tenue |
| `--yellow-text` | `#713f12` | Texto oscuro de alto contraste sobre amarillo tenue |

---

## 3. Explicación del Código

### A. HTML5 Semántico (`index.html`)
- `<header>` y `<nav>`: Encabezado fijo con logotipo `BB` y enlaces a `#inicio`, `#sobre-mi`, `#proyectos`, `#competencias`, `#habilidades` y `#contacto`.
- `<main>` y `<aside>`: Estructura clara con ficha de perfil rápida en el Hero.
- `<article class="project-card">`: Cada tarjeta usa una lista de definición (`<dl>`) con **Desafío, Implementación, Rol, Herramientas, Evidencia y Aprendizaje**.

### B. CSS3 y Rendimiento (`css/estilos.css`)
- **Layouts modernos:** CSS Grid (`hero-layout`, `bento-about`, `projects-grid`, `achievements-grid`, `skills-grid`) y Flexbox (`header-inner`, `filter-bar`, `tag-list`) adaptados a tablet y móvil (`960px` y `720px`).
- **Animaciones a 60 fps:** Solo se animan `transform` (`translate3d`, `scale`, `scaleX`) y `opacity`, evitando relayouts.
- **Accesibilidad:** Enlace de salto (`.skip-link`), foco visible (`:focus-visible`) y soporte de `@media (prefers-reduced-motion: reduce)`.

### C. JavaScript Nativo (`js/script.js`)
1. **Mejora progresiva (`js-ready`):** Garantiza que el contenido siga visible si JS falla.
2. **Barra de progreso:** Actualiza `transform: scaleX(...)` dentro de `requestAnimationFrame`.
3. **`IntersectionObserver`:** Revela `.reveal-block` y marca la sección activa en la navegación.
4. **Filtros de proyectos:** Alterna visibilidad según `data-filter` y `data-category`.
5. **Modal accesible:** Muestra la imagen SVG ampliada y soporta cierre por botón, clic exterior y tecla `Escape`.
6. **Copiado reutilizable:** Un único controlador lee `data-copy-target` para copiar correo o teléfono y mostrar un aviso temporal (`#toast`).
