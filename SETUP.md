# Configurar este template para tu empresa

Sigue esta lista de arriba a abajo. Busca cada token en el proyecto (Cmd+Shift+F o `grep -rn "{{TOKEN}}"`) y reemplázalo en todos los archivos donde aparece.

## 1. Identidad de la empresa
- `{{NOMBRE_EMPRESA}}` — nombre de tu empresa. Aparece en casi todos los agentes y skills.
- `{{DESCRIPCION_EMPRESA}}` — párrafo describiendo a qué se dedica tu empresa y a quién ayuda. Aparece en ~12 archivos de agentes y en README.md.
- `{{ICP}}` — definición de tu cliente ideal (sector, tamaño, dolor principal). Aparece en 7 archivos de agentes.

## 2. Ofertas / productos
- `{{OFERTA_1}}`, `{{OFERTA_2}}`, `{{OFERTA_3}}` — tus 3 ofertas o productos, usados como ejemplos de CTA en todo el contenido (emails, posts, ads, videos). Representan 3 niveles de compromiso creciente (ej. diagnóstico o recurso gratuito → producto pago → aplicación de alto touch). Ajusta la cantidad de ofertas si tu negocio tiene un número distinto — no es obligatorio tener exactamente 3.

## 3. Voz de marca
- `{{TONO_MARCA}}` — adjetivos que describen el tono de tu marca. Aparece principalmente en `skills/qa-brand/qa-brand-SKILL.md` y `README.md`.

## 4. Identidad visual
- `{{PALETA_DEFAULT_NOMBRE}}` — nombre de tu paleta de marca (puedes mantener los valores hex de ejemplo o cambiarlos). Aparece en `skills/diagrams/skill.md`, `skills/openai-images/openai-images-SKILL.md`, `agents/graphic-producer`, `agents/video-producer`, `agents/viz-diagrams`. Si necesitas más de una paleta temática, duplica el bloque de variables en cada archivo.
- `{{LOGO_ARCHIVO}}` / `{{LOGO_RUTA}}` — nombre y ubicación del archivo de tu logo. Aparece en `agents/graphic-producer`, `agents/video-producer`, `skills/diagrams/skill.md`.
- `{{VARIANTES_LOGO_A_EVITAR}}` (opcional) — en `agents/graphic-producer`, lista de otros archivos de logo que existan y no debas usar. Bórralo si no aplica.
- Tipografía: el template usa Poppins como ejemplo (fuente gratuita de Google Fonts). Reemplázala en `agents/graphic-producer`, `agents/video-producer` y `skills/openai-images/openai-images-SKILL.md` si tu marca usa otra.

## 5. Rutas de salida
- `{{CARPETA_OUTPUTS}}` — ruta local donde se guardan las imágenes/videos generados. Aparece en `skills/openai-images/openai-images-SKILL.md`.

## 6. Metadata del plugin
Edita directamente `.claude-plugin/plugin.json` (JSON no soporta comentarios, por eso no lleva tokens con notas inline):
- `description` — describe tu propio "Marketing OS" en una frase.
- `author.email` — tu email de contacto.
- `homepage` — la URL de tu sitio o del repo.
(`name` y `author.name` se dejaron sin cambios a propósito; cambia `name` solo si vas a distribuir esto como plugin/marketplace y necesitas que coincida con el nombre del directorio.)

## 7. README.md
- `{{GITHUB_REPO}}` — tu organización/repo de GitHub, usado en las instrucciones de instalación.

## Nota: skill google-ads
El directorio `skills/google-ads/` está vacío en este template — es una skill sin implementar. Puedes completarla, dejarla vacía, o borrarla según tus necesidades; no es un error.
