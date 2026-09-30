# mariacamilagonzalez.com

Misma base que sebastianortegon.com (layout de dos columnas, toggle EN/ES con `#en` / `#es`, marquee de logos, globo con tour automático), adaptada para Maria Camila González. Un solo `index.html` con CSS y JS inline, sin build step: se despliega igual en GitHub + Vercel.

## Qué cambia frente al sitio de Sebastián
- **Textos EN/ES**: rol, bio, "About me" y metadatos (título, descripción, OG) de Camila. Los textos están en el objeto `I18N` al final de `index.html` (y el inglés también en el HTML como respaldo).
- **Color de acento**: rosa (`--accent: #ef7a96`, `--accent-dark` / `--pin: #e05a7c`) en lugar del ámbar. Para cambiarlo, edita esas variables en `:root` y los dos valores `ACCENT_RGB` / `'#ef7a96'` dentro del script del globo.
- **Logos de clientes**: se quitó Smurfit Kappa (era empleador de Sebastián, no cliente). El resto se mantiene.
- **Certificaciones**: solo Meta, Google y TikTok (las de su CV). La etiqueta dice "Certified in / Certificada en". Si quieres añadir Snapchat, sube `assets/partners/snapchat.png` y añade el `<img>` en `.partners-grid`.
- **Tarjetas del globo**: muestran "Client project / Proyecto con cliente" en lugar de las cifras de ventas aleatorias por ciudad.

## Placeholders que hay que reemplazar
- `assets/img/profile.jpg`: foto de perfil (cuadrada, mínimo 500×500). Ahora mismo tiene las iniciales "MC".
- `assets/og/og-image.jpg`: imagen para compartir el link (1200×630). Tiene nombre, rol y el stat, sin foto.
- `assets/favicon/*`: iniciales "MC" en rosa. Son opcionales.

## CV descargable
- `assets/cv/cvmariacamila_en.pdf` y `assets/cv/cvmariacamila_es.pdf`. El botón descarga el del idioma activo. Cada PDF enlaza a la otra versión vía `mariacamilagonzalez.com/#es` y `/#en`.

## Deploy (igual que el de Sebastián)
1. Crea un repo en GitHub (por ejemplo `cv`) y sube el contenido de esta carpeta.
2. En Vercel: Add New → Project → importa el repo → Framework "Other", sin build.
3. Settings → Domains: añade `mariacamilagonzalez.com` y `www.mariacamilagonzalez.com`, y copia los registros DNS que pida Vercel en el registrador del dominio.
