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
  phone:      "(346) 373-7420",
  phoneHref:  "+13463737420",
  email:      "bids@gileselectricalservices.com",
  license:    "TECL #39885",
  address:    "PO Box 91243, Houston, TX 77291",
  hours:      "Mon–Fri 7:00 AM – 6:00 PM",
  areaShort:  "Houston and the surrounding area",
  areaCities: ["Houston","Katy","Cypress","Spring","The Woodlands", ...]
};
```

Al cambiar esos valores se actualizan automáticamente el teléfono, correo, número de licencia,
dirección, horario y área de cobertura en toda la página (encabezado, hero, contacto y pie de página).

> Teléfono, licencia (TECL #39885), dirección postal y maestro electricista (Hector Giles,
> #709335) vienen del registro del TDLR. La licencia de contratista vence el 01/28/2027 y la
> de maestro electricista el 12/20/2026: al renovarlas, revisa que los números no cambien.
>
> **Pendiente:** el correo `bids@gileselectricalservices.com` es un marcador de posición.
> Reemplázalo por el correo real (o el del dominio, cuando se compre).

## Formulario de contacto
El botón "Send Bid Request" abre el correo del visitante con la solicitud ya redactada
(no necesita backend). Para recibir los envíos en una bandeja sin depender del correo del visitante,
puede conectarse a un servicio como Formspree o Netlify Forms cambiando el manejador `submit`
indicado en los comentarios del código.
