# Bitácora Ampliada y Guía de Autoría para Exposición Oral

Complemento de [`../bitacora_ia.md`](../bitacora_ia.md) con respuestas rápidas para explicar el proyecto en clase.

---

## 1. Preguntas Frecuentes

### ¿Por qué elegiste usar una ficha técnica lateral en lugar de una foto en el Hero?
Porque permite presentar de inmediato los datos esenciales (edad, colegio, enfoque técnico, entrenamiento físico y disponibilidad) sin depender de una fotografía, logrando una estética más técnica y diferenciada.

### ¿Cómo definiste los colores azulados y el amarillo tenue?
En [`../css/estilos.css`](../css/estilos.css), dentro de `:root`, se declararon variables como `--blue-950`, `--blue-900`, `--blue-700`, `--yellow-100`, `--yellow-200` y `--yellow-text`. Cambiar un color en `:root` actualiza todo el sitio automáticamente.

### ¿Cómo funcionan los filtros y las animaciones al hacer scroll?
- **Filtros:** En [`../js/script.js`](../js/script.js), cada botón de filtro compara su atributo `data-filter` con el `data-category` de cada `<article class="project-card">`.
- **Animaciones:** `IntersectionObserver` detecta cuando un `.reveal-block` entra en pantalla y le agrega la clase `.is-visible`, animando únicamente `opacity` y `transform`.

### ¿Cómo evitaste duplicar código en los botones de copiar correo y teléfono?
Ambos botones usan los atributos HTML `data-copy-target` y `data-copy-label`. En `js/script.js`, un único bucle conecta el evento `click` para cualquiera de los dos botones.

---

## 2. Modificaciones Sencillas en Vivo

1. **Ajustar un tono de azul o amarillo:** Modificar las variables en `:root` dentro de `css/estilos.css`.
2. **Sumar una nueva competencia:** Duplicar un bloque `<article class="achievement-card reveal-block">` en `index.html`.
3. **Cambiar un enlace o dato de contacto:** Editar directamente la sección `#contacto` en `index.html`.
