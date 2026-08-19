# Generador de Firma CASCO Safety

Miniaplicación HTML/CSS/JS sin backend, preparada para publicarse con GitHub Pages e incrustarse en Wix.

## Funcionalidad incluida

- Selector de país: Nicaragua, Guatemala y El Salvador.
- Datos editables: nombre, cargo, correo corporativo y teléfono móvil.
- Prefijo móvil, teléfono de oficina y dirección automáticos por país.
- Web global fija: https://www.cascosafetyglobal.com/
- Arte de 28 años en la firma.
- Arte de Poxipol únicamente cuando se selecciona Guatemala.
- Copiar firma con HTML enriquecido.
- Copiar código HTML.
- Descargar un archivo HTML de la firma.
- Vista previa Light / Dark.
- Botones de Manual PDF y Tutorial ya preparados, actualmente deshabilitados hasta recibir las URLs.

## Estructura

```text
firma-casco/
├── index.html
├── README.md
└── assets/
    ├── logo-casco-safety.png
    ├── casco-28-aniversario.gif
    └── poxipol-guatemala.jpg
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo, por ejemplo `firma-casco`.
2. Sube el contenido de esta carpeta a la rama `main`.
3. En GitHub abre **Settings > Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**.
5. Selecciona `main` y la carpeta `/ (root)`.
6. Guarda y espera a que GitHub muestre la URL pública.

La aplicación convierte las rutas de las imágenes a URLs absolutas al generar/copiar la firma, por lo que las imágenes seguirán siendo accesibles desde Gmail una vez que el sitio esté publicado en GitHub Pages.

## Incrustar en Wix

En la landing de Wix agrega un elemento para **Incrustar un sitio / Embed a site** y usa la URL pública de GitHub Pages.

La interfaz es responsive. Ajusta la altura del iframe en Wix para evitar barras de desplazamiento innecesarias.

## Manual y tutorial

En `index.html`, los botones `manualBtn` y `tutorialBtn` están deshabilitados. Cuando estén disponibles las URLs, se pueden habilitar y conectar sin modificar la lógica principal del generador.

## Compatibilidad con Gmail

Los botones **Copiar firma** y **Descargar HTML** deben usarse desde la URL publicada en GitHub Pages. Si `index.html` se abre como un archivo local (`file://`), Gmail no puede acceder a las imágenes de la carpeta `assets` y el generador mostrará una advertencia.

La firma usa una tabla de ancho fijo y estilos inline compatibles con clientes de correo para evitar que el nombre se divida en dos líneas al pegarlo en Gmail.
