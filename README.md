# Vestuario RD Kids

Tienda online de ropa y calzado para niñas y niños de 0 a 15 años, en San Cristóbal, República Dominicana.
Pedidos por WhatsApp: **+1 (809) 940-9400**.

Sitio estático de un solo archivo (`index.html`): no requiere servidor, base de datos ni proceso de compilación.

## Contenido del repositorio

| Archivo      | Función                                                         |
|--------------|-----------------------------------------------------------------|
| `index.html` | La tienda completa: estilos, catálogo, música, carrito y fondo  |
| `.nojekyll`  | Indica a GitHub Pages que publique el archivo tal cual          |
| `README.md`  | Este documento                                                  |

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub (por ejemplo `vestuario-rd-kids`), público.
2. Subir `index.html`, `.nojekyll` y `README.md` a la raíz del repositorio
   (botón **Add file → Upload files**, o con `git push`).
3. Ir a **Settings → Pages**.
4. En **Build and deployment**, elegir *Source: Deploy from a branch*, rama `main`, carpeta `/ (root)`, y guardar.
5. En uno o dos minutos la tienda queda en `https://<usuario>.github.io/vestuario-rd-kids/`.

Con Git desde la terminal:

```bash
git init
git add index.html .nojekyll README.md
git commit -m "Tienda Vestuario RD Kids"
git branch -M main
git remote add origin https://github.com/<usuario>/vestuario-rd-kids.git
git push -u origin main
```

## Actualizar productos y fotos (modo dueña)

1. Abrir la tienda publicada y tocar el candado del menú superior.
2. Ingresar la clave de la dueña, editar productos o subir fotos desde la cámara del celular.
3. Tocar **Publicar cambios**: se descarga un `index.html` nuevo con los cambios ya incluidos.
4. Subir ese `index.html` al repositorio, reemplazando el anterior. GitHub Pages actualiza la tienda en uno o dos minutos.

## Funciones

- Foto de la tienda como fondo permanente, con movimiento suave; los productos son transparentes y dejan ver la tienda.
- Cuatro bachatas sintetizadas que se alternan cada 60 segundos (suave, romántica, amargue y alegre).
- Departamentos Niñas y Niños, filtros por edad, búsqueda, carrito y pedido directo por WhatsApp.
- Recorrido guiado por las vitrinas.
- Modo claro y oscuro automático; diseño adaptado a celular.

## Consideraciones técnicas

- **Clave de la dueña.** Está escrita dentro de `index.html` (variable `OWNER_KEY`), por lo que cualquier persona que vea el código fuente puede leerla. Sirve para evitar ediciones accidentales, no como seguridad real. Antes de publicar, conviene cambiarla por una propia.
- **Fotos.** Las fotos subidas quedan incrustadas dentro de `index.html`. Muchas fotos aumentan el tamaño del archivo; GitHub admite archivos de hasta 100 MB, pero para una carga rápida conviene mantenerlo bajo 10–15 MB.
- **Carrito y preferencias.** Se guardan solo en el navegador de cada clienta (`localStorage`).
- **Música.** Por política de los navegadores, comienza después del primer toque en la página.
- **Siguiente etapa.** Para que la dueña actualice el catálogo en línea sin volver a subir archivos, el paso natural es conectar la tienda a una base de datos como Supabase.
