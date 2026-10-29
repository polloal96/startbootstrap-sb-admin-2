# Giles Electrical Services — Sitio web (archivo único)

`index.html` es la página completa: HTML, CSS, JavaScript, el logo y las seis fotos de obra
van incrustados dentro del mismo archivo (~1.9 MB). No requiere servidor ni configuración.

## Publicar
1. Sube `index.html` a la carpeta raíz de tu hosting (`public_html`, `www` o equivalente).
2. Listo. Funciona con cualquier hosting estático (cPanel, Netlify, GitHub Pages, Hostinger, etc.).

## Actualizar los datos del negocio
Abre `index.html` con cualquier editor de texto y busca el bloque `CONFIG` al final del archivo:

```js
var CONFIG = {
  phone:      "(512) 555-0199",
  phoneHref:  "+15125550199",
  email:      "bids@gileselectricalservices.com",
  license:    "TECL #00000",
  city:       "Austin, Texas",
  hours:      "Mon–Fri 7:00 AM – 6:00 PM",
  areaShort:  "Central Texas and statewide",
  areaCities: ["Austin","San Antonio","Houston", ...]
};
```

Al cambiar esos valores se actualizan automáticamente el teléfono, correo, número de licencia,
ciudad, horario y área de cobertura en toda la página (encabezado, hero, contacto y pie de página).

> Los valores actuales son marcadores de posición. Reemplaza especialmente `license`
> con el número real de licencia TECL emitido por el TDLR antes de publicar.

## Formulario de contacto
El botón "Send Bid Request" abre el correo del visitante con la solicitud ya redactada
(no necesita backend). Para recibir los envíos en una bandeja sin depender del correo del visitante,
puede conectarse a un servicio como Formspree o Netlify Forms cambiando el manejador `submit`
indicado en los comentarios del código.
