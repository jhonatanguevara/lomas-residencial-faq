# Edificio LOMAS RESIDENCIAL — Portal Web

Sitio estático listo para desplegar en **GitHub Pages**, **Netlify** o **Vercel**.

---

## Estructura de carpetas

```
/
├── index.html                         ← Archivo principal del sitio
├── assets/
│   ├── anuncios/                      ← Imágenes PNG del hero / anuncios principales
│   ├── notificaciones/
│   │   ├── inmobiliaria/              ← PNGs de anuncios de la inmobiliaria
│   │   └── administracion/            ← PNGs de anuncios de administración
└── README.md
```

---

## Cómo agregar contenido

### Anuncios y notificaciones (PNG)
1. Sube las imágenes PNG a la carpeta correspondiente.
2. En `index.html`, dentro de la sección `anuncios` o `notificaciones`, cambia el bloque:
   ```html
   <div class="notice-placeholder">...</div>
   ```
   por una etiqueta de imagen:
   ```html
   <img src="assets/anuncios/mi-anuncio.png" alt="Descripción" style="width:100%">
   ```

### Acuerdos / minutas
En la tabla de la sección `#acuerdos`, rellena la fecha, nombre del documento y pega el link de Google Drive en `href`.

### Presupuesto de mantenimiento
Reemplaza los valores de la tabla de la sección `#mantenimiento` con los datos del Excel.

### Áreas comunes
Completa los costos y pega los links de Drive en cada botón "Descargar formato".

### FAQ
Duplica este bloque para cada nueva pregunta:
```html
<details>
  <summary>Pregunta aquí</summary>
  <p>Respuesta aquí</p>
</details>
```

---

## Despliegue gratuito

### GitHub Pages (recomendado)
1. Sube el proyecto a un repositorio en GitHub.
2. Ve a **Settings → Pages**.
3. Selecciona la rama principal y carpeta raíz (`/`).
4. El sitio queda disponible en `https://tu-usuario.github.io/nombre-repo`.

### Netlify
1. Arrastra la carpeta del proyecto al panel de Netlify.
2. El sitio queda publicado al instante con URL pública.

### Vercel
1. Conecta el repositorio de GitHub en vercel.com.
2. Despliega con clic único.

---

## Próximas mejoras posibles
- Subir el Excel de mantenimiento para autocompletar la tabla de presupuesto.
- Agregar todas las FAQ del PDF.
- Implementar filtro de búsqueda en la sección FAQ (solo JS, sin dependencias).
