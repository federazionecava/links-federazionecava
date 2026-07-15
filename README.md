# 🦁 Linktree · Federazione CAVA

Página de enlaces (estilo "link in bio") para el **Comitato delle Associazioni Venete dell'Argentina**, pensada para escanear vía QR y usar principalmente desde el celular.

Hecha en **HTML + CSS puro**, sin frameworks ni dependencias — liviana, fácil de editar y de hostear en cualquier lado.


---

## 📁 Estructura del proyecto

```
.
├── index.html   → Estructura de la página (contenido, textos, links)
└── style.css    → Todos los estilos (colores, tipografía, layout, animaciones)
```

---

## 🚀 Cómo publicarlo / actualizarlo

1. Abrí `index.html` en el navegador para ver los cambios en el momento (doble clic alcanza).
2. Para publicarlo online, guardá los cambios, publicalo y el link original va a andar siempre.
3. Apuntá el código QR a la URL final una vez publicado.

---

## 🛠️ Cómo editar lo más común

### Cambiar un link o agregar uno nuevo
Los enlaces viven dentro de `<div class="links">` en `index.html`. Cada uno sigue esta estructura:

```html
<a class="link" href="URL_ACA" target="_blank" rel="noopener">
  <svg viewBox="0 0 24 24">...</svg>
  Texto visible
</a>
```

Para agregar una red nueva, copiá un bloque `<a class="link">` existente, cambiá el `href`, el texto, y el ícono SVG de adentro (hay miles de íconos gratuitos en [Lucide](https://lucide.dev/icons/) o [Material Symbols](https://fonts.google.com/icons), buscá "outline" o "filled" según el estilo que uses).

> ⚠️ Importante: el mail usa `href="mailto:direccion@mail.com"` en vez de una URL normal — no lleva `target="_blank"`.

### Cambiar nombre, subtítulo o logo
Están arriba de todo en `index.html`, antes de `<div class="links">`. El logo es una imagen (`<img>`) dentro de un contenedor circular — para cambiarlo, solo hay que reemplazar el `src`.

### Cambiar colores
Todos los colores están centralizados como **variables CSS** al inicio de `style.css`, dentro de `:root`. Por ejemplo:

```css
:root{
  --texto: ...;
  --crema: ...;
  --crema-2: ...;
  --laguna: ...;
  --oro: ...;
}
```

Cambiando el valor de una variable ahí, se actualiza en todo el sitio automáticamente — no hace falta tocar el resto del CSS.

---

## 🤝 Si algún día alguien más retoma esto

Este sitio fue armado para ser **lo más simple de mantener posible**, incluso para alguien sin experiencia en programación:

- No hay que instalar nada ni correr comandos — es abrir el archivo y editar texto.
- Todo el contenido (textos, links, colores) está a la vista en dos archivos, sin lógica oculta ni configuración externa.
- Si algo se rompe visualmente, el 90% de las veces alcanza con revisar que no falte cerrar una etiqueta (`<a>`, `<div>`, `<svg>`) o una llave `{ }` en el CSS.

Cualquier duda sobre una sección puntual, los comentarios dentro del propio `style.css` y `index.html` deberían guiar bastante.

---
<p align="center">
  <sub>Hecho con ❤️ para la Federazione CAVA — por <a href="https://github.com/wurst-bruno">@wurst-bruno</a></sub>
</p>
