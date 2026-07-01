---
name: openai-images
description: Genera imágenes reales con DALL-E 3 de OpenAI a partir de un brief visual. Úsalo cuando graphic-producer necesite producir ads, carruseles, banners o cualquier pieza gráfica de Rocket Revenue. Requiere OPENAI_API_KEY en el entorno.
---

# openai-images

Genera imágenes con DALL-E 3 a partir de un brief visual y las guarda en la carpeta de outputs de la campaña.

---

## Flujo de trabajo

### Paso 1 — Leer el brief

Extrae del brief visual:
- Mensaje principal
- Canal y formato (feed, story, banner, etc.)
- Estilo visual (limpio, bold, minimalista)
- Paleta de colores
- Elementos visuales requeridos
- Qué evitar

### Paso 2 — Construir el prompt para DALL-E 3

Traduce el brief a un prompt en inglés optimizado para DALL-E 3.

**Estructura del prompt:**
```
[Estilo visual] [Composición] for [canal/formato]. [Mensaje o concepto visual]. [Paleta de colores]. [Tipografía si aplica]. [Elementos a incluir]. [Elementos a evitar]. Professional B2B marketing visual. Clean, high contrast, no text overlays.
```

**Reglas para el prompt:**
- Siempre en inglés (DALL-E responde mejor)
- Ser específico con colores: usar hex o nombres exactos ("dark navy #1A2340", "amber #F59E0B")
- Pedir "no text" si el copy va a agregarse después en Canva
- Especificar "professional B2B", "corporate", "clean" para evitar estilos consumer
- Máximo 400 caracteres para mayor precisión

**Ejemplo de prompt:**
```
Minimalist professional B2B marketing banner. Abstract geometric shapes suggesting growth and systems on dark navy background #1A2340. Amber accent #F59E0B geometric lines. Clean, corporate, high contrast. No people, no text, no stock photography clichés. Suitable for LinkedIn or Instagram feed.
```

### Paso 3 — Determinar el tamaño

DALL-E 3 soporta estos tamaños. Elige el más cercano al formato del brief:

| Formato solicitado | Tamaño DALL-E 3 |
|---|---|
| Feed cuadrado 1:1 (1080×1080) | `1024x1024` |
| Feed vertical 4:5 (1080×1350) | `1024x1792` |
| Story/Reel 9:16 (1080×1920) | `1024x1792` |
| Banner horizontal 16:9 | `1792x1024` |
| LinkedIn banner | `1792x1024` |
| Thumbnail video | `1792x1024` |

### Paso 4 — Llamar a la API

Ejecuta este comando Bash para generar la imagen:

```bash
curl -s https://api.openai.com/v1/images/generations \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -d "{
    \"model\": \"dall-e-3\",
    \"prompt\": \"PROMPT_AQUI\",
    \"n\": 1,
    \"size\": \"TAMAÑO_AQUI\",
    \"quality\": \"hd\",
    \"style\": \"natural\"
  }"
```

La respuesta incluye una URL temporal de la imagen generada en `.data[0].url`.

### Paso 5 — Descargar y guardar la imagen

Con la URL del paso anterior, descarga y guarda la imagen:

```bash
curl -s "URL_DE_LA_IMAGEN" -o "RUTA_DE_DESTINO/nombre-archivo.png"
```

**Convención de nombres:**
```
[campaña]-[tipo]-[descripción]-v1.png
```

Ejemplos:
- `diagnostico-revenue-ad-meta-dolor-v1.png`
- `grancalendario-banner-linkedin-v1.png`
- `vendex-story-ig-cta-v1.png`

**Carpeta de destino:**
```
/Users/diegomorales/Documents/Claude/Projects/[nombre-campaña]/outputs/[nombre-campaña]/imagenes/
```

### Paso 6 — Reportar resultado

Al terminar cada imagen entrega:
1. Ruta completa del archivo guardado
2. El prompt exacto usado (para poder iterar)
3. Notas si hubo alguna decisión no cubierta por el brief

---

## Generar variantes

Para testear ángulos distintos, genera 2-3 variantes cambiando:
- El estilo: `"style": "natural"` vs `"style": "vivid"`
- La composición del prompt (más abstracto vs más literal)
- El color dominante

Nombra las variantes con `-v1`, `-v2`, `-v3`.

---

## Calidad recomendada

Siempre usa `"quality": "hd"` para piezas de campaña. Solo usa `"quality": "standard"` para borradores rápidos de revisión.

---

## Checklist antes de entregar

- [ ] ¿El prompt está en inglés?
- [ ] ¿El tamaño es el más cercano al formato solicitado?
- [ ] ¿La imagen se guardó en la carpeta correcta?
- [ ] ¿El nombre del archivo sigue la convención?
- [ ] ¿Se reportó la ruta y el prompt usado?

---

## Notas importantes

- DALL-E 3 no puede generar texto legible dentro de imágenes — si la pieza necesita copy encima, genera el fondo/composición visual y el copy se agrega después en Canva o Figma.
- Si la API devuelve error de contenido, reformula el prompt removiendo términos que puedan ser ambiguos.
- Las URLs de imagen que devuelve OpenAI expiran en 1 hora — siempre descarga y guarda localmente de inmediato.
