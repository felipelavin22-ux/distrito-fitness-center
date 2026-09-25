# Distrito Fitness Center

Landing page institucional para **Distrito Fitness Center**, gimnasio ubicado en Caballito, Ciudad Autónoma de Buenos Aires. Presenta las disciplinas del centro (Musculación, CrossFit, Hyrox y Calistenia), instalaciones, convenio con WellHub y vías de contacto.

**Sitio en vivo:** https://felipelavin22-ux.github.io/distrito-fitness-center/

## Stack

- HTML5 semántico
- [Tailwind CSS](https://tailwindcss.com/) (vía CDN — sin build step)
- JavaScript vanilla (animaciones, scroll reveal, contador de sector "En números")
- [Lucide Icons](https://lucide.dev/) v1.45.0 (vía unpkg, versión fijada)
- Google Fonts: Archivo + Inter

No requiere `npm install` ni build: es un sitio estático puro.

## Estructura del proyecto

```
├── index.html              # Página principal (todo el sitio en un solo archivo)
├── privacidad.html          # Política de Privacidad
├── terminos.html             # Términos y Condiciones
├── cookies.html               # Política de Cookies
├── robots.txt                # Reglas de rastreo para buscadores
├── sitemap.xml                # Sitemap para Google Search Console
├── logo_distrito.png          # Logo del gimnasio
├── wellhub_logo.png            # Logo del convenio WellHub
├── video-encabezado.mp4         # Video de fondo del hero
└── assets/
    ├── sector02-gym.png         # Foto de instalaciones
    ├── cafeteria-hover.mp4       # Video hover de la cafetería
    ├── disciplinas/               # Imágenes de cada disciplina
    └── vestuario/                  # Imágenes de vestuarios
```

## Cómo correrlo en local

Al ser un sitio estático, alcanza con abrir `index.html` en el navegador. Para evitar restricciones de CORS con las rutas relativas de video/imágenes, es preferible levantar un servidor local simple:

```bash
# Con Python
python3 -m http.server 5500

# Con Node (npx)
npx serve .
```

Luego abrir `http://localhost:5500`.

## Despliegue

El sitio se publica con **GitHub Pages** desde la rama `main` de este repositorio. Cualquier cambio en `main` se refleja automáticamente en producción entre 30 segundos y unos minutos después del push.

## Seguridad

El sitio incluye una política de `Content-Security-Policy` (CSP) restrictiva vía meta tag, que solo permite cargar scripts/estilos desde Tailwind CDN, unpkg (Lucide) y Google Fonts. Esto reduce el riesgo de inyección de scripts maliciosos de terceros.

## Recursos de terceros / tracking

Este sitio **no** utiliza cookies, `localStorage` ni herramientas de analítica (Google Analytics, Meta Pixel, Microsoft Clarity, etc.) a la fecha de este README. Las únicas conexiones a servidores externos son:

- Tailwind CSS (CDN)
- Google Fonts
- Lucide Icons (unpkg)

Si en el futuro se agrega Google Analytics 4 o Microsoft Clarity, hay que:
1. Actualizar `cookies.html` y `privacidad.html` en consecuencia.
2. Sumar el dominio del script correspondiente a la política CSP (`script-src`) en `index.html`.

## SEO y buscadores

- `robots.txt` permite la indexación de `index.html` y bloquea las páginas legales (no aportan valor de búsqueda).
- `sitemap.xml` declara la URL principal.
- Pendiente tras cada despliegue relevante: dar de alta el sitio en [Google Search Console](https://search.google.com/search-console), enviar el sitemap y solicitar indexación manual de la home.

## Propiedad del contenido

El código de este sitio fue desarrollado por **Felipe Lavin Piriz** como servicio freelance para Distrito Fitness Center. La marca, el logo, las fotografías de instalaciones y los textos institucionales son propiedad de Distrito Fitness Center. Los términos de uso, licencia y alcance del trabajo realizado se detallan en el contrato de servicios correspondiente (fuera de este repositorio).

## Contacto

- **Desarrollador:** Felipe Lavin Piriz — [felipelavin22-ux.github.io](https://felipelavin22-ux.github.io/)
- **Cliente:** Distrito Fitness Center — distritofitnesscenter@gmail.com
