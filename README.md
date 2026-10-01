# Diseridú · Tienda web

Tienda mobile-first de remeras y stickers. Es un solo `index.html` con las imágenes en `img/`, sin build ni dependencias.

## Publicar en GitHub Pages
1. Subí `index.html`, `README.md` y la carpeta `img/` a la raíz del repo.
2. En el repo: **Settings → Pages → Deploy from a branch → main / (root)**.
3. A los minutos queda en `https://<usuario>.github.io/<repo>/`.

## Editar
Todo lo editable está al principio del `<script>` en `index.html`:
- `WHATSAPP`: número con código de país, sin + ni espacios (hoy `5491125843143`).
- `PRODUCTOS`: nombre, precio (`null` = "Consultá precio"), descripción y fotos de cada diseño.
- `TALLES`: lista de talles disponibles.

Para sumar una remera, agregá dos fotos en `img/` (`nombre-blanca.jpg` y `nombre-negra.jpg`) y una entrada nueva en `PRODUCTOS`.

## Tu diseño (generador de estampas)
En `#tu-diseno` el cliente sube su imagen, la mueve y escala sobre la remera (blanca o negra), ve el tamaño aproximado en cm y la resolución en ppp, descarga el mockup y consulta por WhatsApp. Las fotos base son `img/base-blanca.jpg` y `img/base-negra.jpg`; el área de impresión se ajusta con `ZONA` y la escala en cm con `ANCHO_FOTO_CM`.

Cada producto tiene un botón "Consultar por WhatsApp" que abre el chat con el producto, color, talle y cantidad ya escritos.
