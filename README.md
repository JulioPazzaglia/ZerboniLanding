# Yo Sumo — Ampliación Área Crítica Hospital Zerboni

Landing de donaciones para la campaña "Yo Sumo" del Hospital Municipal Emilio Zerboni (San Antonio de Areco, Buenos Aires).

## Cómo publicar en GitHub Pages

1. Creá un repositorio nuevo en GitHub (público, para que Pages sea gratis) y subí el contenido de esta carpeta a la rama `main`.
2. En el repo: **Settings → Pages**.
3. En **Source**, elegí `Deploy from a branch`.
4. En **Branch**, elegí `main` y la carpeta `/ (root)`.
5. Guardá. GitHub te va a dar una URL del tipo:
   `https://<tu-usuario>.github.io/<nombre-del-repo>/`
6. Puede tardar 1-2 minutos en quedar activa.

## Antes de publicar

Abrí `index.html`, buscá el bloque `<script>` cerca del final y editá:

```js
const DONAR_ONLINE_URL = "https://donaronline.org/"; // reemplazar por el link real de la campaña
const METROS = [ ... ]; // confirmar si los montos siguen vigentes
```

## Dominio propio (opcional)

Si más adelante querés usar un dominio propio (ej. `yosumo.hospitalzerboni.org`):
1. Agregá un archivo `CNAME` en la raíz con el dominio adentro (una sola línea).
2. Configurá el DNS del dominio con un registro `CNAME` apuntando a `<tu-usuario>.github.io`.
3. En Settings → Pages, ingresá el dominio en "Custom domain".

## Estructura

```
zerboni-landing/
├── index.html
└── images/
    ├── logo.jpg
    ├── hero-acceso.jpg
    ├── render-aereo.jpg
    ├── render-aereo-techo.jpg
    ├── render-exterior-frontal.jpg
    ├── render-exterior-lateral.jpg
    ├── render-interior-uci.jpg
    ├── foto-obra-avance.jpg
    └── foto-obra-interior.jpg   (sin usar en el layout actual, disponible para sumar)
```

`index.html` es HTML + CSS + JS plano (sin build), y las imágenes se referencian por ruta relativa (`images/...`), no en base64. No requiere dependencias.
