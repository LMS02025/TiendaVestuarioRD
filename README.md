# Vestuario RD Kids

Tienda online de artículos para bebé, niñas y niños, en San Cristóbal, República Dominicana.
Pedidos por WhatsApp: **+1 (809) 940-9400**.

Eslogan: *Visita tu tienda y viste a tu gusto.*

Sitio estático: no requiere servidor, base de datos ni proceso de compilación.

## Contenido del repositorio

| Archivo / carpeta | Función                                                                 |
|-------------------|-------------------------------------------------------------------------|
| `index.html`      | La tienda completa: estilos, catálogo (528 artículos), música y carrito |
| `img/v0…v8.webp`  | Fotos del catálogo agrupadas en 9 láminas (64 fotos de 300 × 300 px c/u) |
| `.nojekyll`       | Indica a GitHub Pages que publique los archivos tal cual                 |
| `README.md`       | Este documento                                                           |

`index.html` y la carpeta `img/` deben quedar juntos en la raíz del repositorio.

## Publicar en GitHub Pages

1. Ir a **Settings → Pages** del repositorio.
2. En **Build and deployment**, elegir *Source: Deploy from a branch*, rama `main`, carpeta `/ (root)`, y guardar.
3. En uno o dos minutos la tienda queda en `https://lms02025.github.io/TiendaVestuarioRD/`.

## Funciones

- Foto de la tienda como fondo permanente, con movimiento suave; paneles y menús de vidrio transparente.
- Vitrina de portada con tres ventanas (Niñas, Bebé, Niños), cada una con 5 productos reales que rotan.
- Catálogo de 528 artículos en 17 secciones, con filtro por sección, por niña / niño y búsqueda por nombre o código `VR-`.
- Cada artículo muestra su nombre y código; el precio es "a consultar" hasta que la dueña lo defina.
- Carrito y pedido directo por WhatsApp (sin cobro de envío ni pasarela de pago).
- Música de fondo: una bachata suave sintetizada; efectos de sonido opcionales.
- Recorrido guiado por todas las secciones.
- Modo claro y oscuro automático; diseño adaptado a celular.

## Actualizar precios, nombres y fotos (modo dueña)

1. Abrir la tienda publicada y tocar el candado del menú superior.
2. Ingresar la clave, tocar el lápiz de un producto y cambiar precio, nombre o foto
   (la foto puede tomarse con la cámara del celular; se recorta y ajusta automáticamente).
3. Tocar **Publicar cambios**: se descarga un `index.html` nuevo con los cambios incluidos.
4. Subir ese `index.html` al repositorio (**Add file → Upload files**), reemplazando el anterior.
   GitHub Pages actualiza la tienda en uno o dos minutos.

## Códigos de producto

Los códigos visibles usan el prefijo `VR-`. Corresponden uno a uno con el código del proveedor
cambiando el prefijo (por ejemplo, `VR-11578` ↔ `CO-11578`).

## Consideraciones técnicas

- **Clave de la dueña.** Está escrita dentro de `index.html` (variable `OWNER_KEY`); cualquiera que vea
  el código fuente puede leerla. Sirve para evitar ediciones accidentales, no como seguridad real.
  Conviene cambiarla por una propia antes de compartir el enlace.
- **Fotos nuevas de la dueña.** Quedan incrustadas dentro de `index.html` (720 × 720 px). Muchas fotos
  aumentan el tamaño del archivo; conviene mantenerlo bajo 10–15 MB para una carga rápida.
- **Fotos del catálogo.** Se retiraron el logo y la ficha técnica impresos sobre las fotos. La marca
  impresa en los empaques de algunos productos sigue visible; para ocultarla, reemplazar esas fotos
  por fotos propias desde el modo dueña.
- **Carrito y preferencias.** Se guardan solo en el navegador de cada clienta (`localStorage`).
- **Música.** Por política de los navegadores, comienza después del primer toque en la página.
- **Siguiente etapa.** Para que la dueña actualice el catálogo en línea sin volver a subir archivos,
  el paso natural es conectar la tienda a una base de datos como Supabase.
