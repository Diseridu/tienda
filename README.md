# Diseridú · Tienda web

Tienda mobile-first de remeras, tote bags y encendedores. Es un solo `index.html` con las imágenes en `img/`, sin build ni dependencias.

## Publicar en GitHub Pages
1. Subí `index.html`, `README.md` y la carpeta `img/` a la raíz del repo.
2. En el repo: **Settings → Pages → Deploy from a branch → main / (root)**.
3. A los minutos queda en `https://<usuario>.github.io/<repo>/`.

## Editar la tienda
Entrá a `https://diseridu.github.io/tienda/#editar` (mejor desde la compu). Ahí podés:
- cambiar fotos, nombres, etiquetas, precios y descripciones,
- ordenar, agregar o borrar remeras, tote bags y encendedores,
- cambiar el WhatsApp y el Instagram.

Cuando termines, tocá **Descargar index.html** y en GitHub subí ese archivo reemplazando el `index.html` actual. Las fotos nuevas quedan guardadas dentro del mismo archivo, así que no hace falta subir nada a `img/`.

Si preferís editar a mano, los datos están en el bloque `<script id="datos-tienda" type="application/json">` del `index.html`.

## Encendedor 3D
En `#encendedor-3d` (botón "Armá tu fuego en 3D" dentro de Encendedores) el cliente elige un diseño de la tienda o sube el suyo, lo ve pegado en un encendedor 3D, cambia el color, descarga la imagen y consulta por WhatsApp. Usa Three.js desde CDN y solo se carga al abrir esa vista. Los diseños que ofrece están en `E3D_DISENOS` (imágenes `img/e3d-*.jpg`).

## Tu diseño (generador de estampas)
En `#tu-diseno` el cliente sube su imagen, la mueve y escala sobre la remera (blanca o negra), ve el tamaño aproximado en cm y la resolución en ppp, descarga el mockup y consulta por WhatsApp. Las fotos base son `img/base-blanca.jpg` y `img/base-negra.jpg`; el área de impresión se ajusta con `ZONA` y la escala en cm con `ANCHO_FOTO_CM`.

Cada producto tiene un botón "Consultar por WhatsApp" que abre el chat con el producto, color, talle y cantidad ya escritos.
