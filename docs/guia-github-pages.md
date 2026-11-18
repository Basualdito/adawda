# Guía Paso a Paso: Publicación en GitHub Pages

Guía para subir el portfolio de **Braian Nahuel Basualdo** a GitHub y publicarlo con **GitHub Pages**.

---

## 1. Crear o Verificar la Cuenta de GitHub

1. Ingresá a [https://github.com/](https://github.com/).
2. Creá tu cuenta (o iniciá sesión) usando un nombre de usuario claro (por ejemplo: `braianbasualdo` o `brabasualdo`).

---

## 2. Crear el Repositorio Público

1. Hacé clic en **New repository**.
2. En **Repository name**, escribí:
   ```text
   tuusuario.github.io
   ```
3. Seleccioná visibilidad **Public** y presioná **Create repository**.

---

## 3. Subir los Archivos del Proyecto

### Opción A: Desde la web de GitHub
1. Abrí tu repositorio y elegí **Add file → Upload files**.
2. Subí **el contenido interno** de la carpeta `BASUALDO/` para que `index.html` quede en la raíz:
   - `index.html`
   - `README.md`
   - `bitacora_ia.md`
   - `css/estilos.css`
   - `js/script.js`
   - `assets/img/*.svg`
   - `docs/*`
3. Confirmá con **Commit changes**.

### Opción B: Desde la terminal (Git)
```bash
git init
git add index.html README.md bitacora_ia.md css/ js/ assets/ docs/
git commit -m "Versión inicial del portfolio personal"
git branch -M main
git remote add origin https://github.com/tuusuario/tuusuario.github.io.git
git push -u origin main
```

---

## 4. Activar GitHub Pages

1. Entrá a **Settings → Pages**.
2. En **Source**, elegí **Deploy from a branch**.
3. En **Branch**, seleccioná `main` y la carpeta `/(root)`, luego presioná **Save**.
4. Esperá de 1 a 3 minutos y abrí `https://tuusuario.github.io`.

---

## 5. Pruebas Posteriores

- [ ] Verificar que `index.html` y `docs/index.html` carguen sin errores 404.
- [ ] Probar todos los enlaces del menú superior y los filtros de proyectos (`Todos`, `Robótica`, `Páginas Web`, `Diseño de Apps`).
- [ ] Abrir el modal de evidencia visual de los 4 proyectos y cerrarlo con `Escape`.
- [ ] Probar los botones **Copiar correo** y **Copiar teléfono**.
- [ ] Revisar en celular que no haya scroll horizontal ni textos cortados.
