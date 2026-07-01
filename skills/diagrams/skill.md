---
name: diagrams
description: Genera diagramas y visuales como SVG o HTML con las paletas de marca, tipografía Poppins y los estilos visuales de Rocket Revenue. Úsalo para frameworks, embudos, comparativas, procesos, matrices y cualquier visual explicativo.
---

# Skill: Diagrams & Visuals

Cuando este skill se invoque, genera diagramas y visuales como código SVG o HTML autocontenido, listos para abrir en browser, exportar a PNG o incrustar en Notion/Canva.

## Tipografía

**Fuente principal:** Poppins (Google Fonts)
Siempre importar al inicio del HTML:
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
```
O en SVG, declarar:
```svg
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');
  * { font-family: 'Poppins', sans-serif; }
</style>
```

Pesos a usar:
- Títulos: 700 (Bold)
- Subtítulos / labels: 600 (SemiBold)
- Cuerpo / descripciones: 400 (Regular)
- Texto secundario: 300 (Light)

---

## Paletas disponibles

### Paleta 1 · Navy + Magenta ← PREDETERMINADA
> Usar por defecto salvo que se indique otra.

```
--bg:        #0A1A3C   (fondo principal)
--card:      #10234D   (tarjetas, paneles)
--card-alt:  #16284F   (tarjetas alternativas)
--accent:    #E0218A   (magenta — acento principal, CTAs, highlights)
--border:    #2A3F6E   (bordes y separadores)
--text-sec:  #9FB0D4   (texto secundario)
--text-faint:#5E6F94   (texto terciario / hints)
--title:     #FFFFFF   (títulos y texto principal)
--accent-lt: #FBD0E6   (texto sobre fondos magenta)
```

### Paleta 2 · Terminal Mint
> Dev, automatización, Claude Code, RevOps técnico.

```
--bg:        #13131A
--card:      #1C1C26
--accent:    #00D4AA
--border:    rgba(0,212,170,0.2)
--text-sec:  #94A3B8
--title:     #FFFFFF
```

### Paleta 3 · Azul Eléctrico
> Data, finanzas, B2B analytics, revenue metrics.

```
--bg:        #0B1437
--card:      #13205A
--accent:    #3B82F6
--accent-2:  #60A5FA
--border:    #26356E
--text-sec:  #94A8D0
--title:     #FFFFFF
```

### Paleta 4 · Morado Profundo
> Estrategia, IA, innovación, thought leadership.

```
--bg:        #1A0B2E
--card:      #2A1A45
--accent:    #A855F7
--accent-2:  #C084FC
--border:    #3D2A5C
--text-sec:  #B0A0CE
--title:     #FFFFFF
```

### Paleta 5 · Índigo + Cian
> SaaS, growth, producto, go-to-market.

```
--bg:        #0F1235
--card:      #1B1F4D
--accent:    #6366F1
--accent-2:  #22D3EE
--border:    #2A2F66
--text-sec:  #9CA3D4
--title:     #FFFFFF
```

---

## Tipos de visual que puedes generar

Elige el tipo que mejor represente la estructura real del contenido. No elijas por preferencia estética — elige por la lógica del dato.

### 1. Funnel / Embudo
**Cuándo:** Proceso con reducción progresiva entre etapas.
**Ejemplo:** Leads → MQL → SQL → Oportunidad → Cliente.
**Forma:** Trapecios apilados de mayor a menor, porcentajes o volúmenes en cada etapa.

### 2. Pipeline Horizontal
**Cuándo:** Etapas secuenciales sin reducción, mismo peso visual.
**Ejemplo:** Sales stages, proceso de onboarding, hiring process.
**Forma:** Cajas o flechas encadenadas horizontalmente, mismo tamaño cada etapa.

### 3. Journey Map
**Cuándo:** Experiencia del cliente en el tiempo con emociones, canales y touchpoints.
**Ejemplo:** Customer journey B2B: descubrimiento → evaluación → compra → adopción.
**Forma:** Fila de fases con filas de canales, emociones y acciones por columna.

### 4. Mapa de Relaciones / Diagrama de Actores
**Cuándo:** Múltiples actores o sistemas con conexiones entre ellos.
**Ejemplo:** RevOps: cómo se conectan Marketing, Ventas, CS y el CRM.
**Forma:** Nodos conectados por líneas con etiquetas en las conexiones.

### 5. Comparativa en Columnas
**Cuándo:** Contrastar 2–4 opciones, enfoques o frameworks en las mismas dimensiones.
**Ejemplo:** Inbound vs Outbound, Producto-Led vs Sales-Led, Free vs Pro vs Enterprise.
**Forma:** Columnas paralelas con las mismas filas de criterios, highlights en la opción recomendada.

### 6. Árbol / Jerarquía
**Cuándo:** Taxonomías, estructuras organizacionales, descomposición de categorías.
**Ejemplo:** ICP: industrias → segmentos → arquetipos. OKRs → Key Results → Iniciativas.
**Forma:** Nodo raíz en la cima, ramas hacia abajo, hojas al final.

### 7. Ciclo / Flywheel
**Cuándo:** Procesos repetitivos donde cada etapa alimenta a la siguiente.
**Ejemplo:** HubSpot Flywheel, ciclo de feedback producto, loop de referidos.
**Forma:** Círculo continuo con etapas en los arcos y flechas de dirección.

### 8. Matriz 2×2
**Cuándo:** Segmentación o priorización en dos ejes independientes.
**Ejemplo:** Impacto vs Esfuerzo, Urgencia vs Importancia, segmentos por tamaño y madurez.
**Forma:** Cuatro cuadrantes con ejes etiquetados, ítems posicionados dentro de cada cuadrante.

### 9. Timeline / Roadmap
**Cuándo:** Evolución en el tiempo, fases de proyecto, hitos históricos.
**Ejemplo:** Roadmap de implementación RevOps, evolución del mercado, milestones de una cuenta.
**Forma:** Línea horizontal o vertical con hitos marcados y descripciones.

### 10. Iceberg / Capas
**Cuándo:** Mostrar lo visible vs lo oculto, o niveles de profundidad de un concepto.
**Ejemplo:** Por qué se pierden deals (síntomas visibles vs causas raíz), deuda técnica.
**Forma:** Sección superior (visible, pequeña) y sección inferior (oculta, grande), línea de agua divisoria.

### 11. Swimlane / Carril por Actor
**Cuándo:** Proceso donde distintos equipos o roles tienen responsabilidades paralelas.
**Ejemplo:** Handoff Marketing → Ventas → CS, proceso de aprobación con múltiples stakeholders.
**Forma:** Filas horizontales por actor, pasos del proceso avanzan de izquierda a derecha con flechas entre carriles.

### 12. Pirámide
**Cuándo:** Jerarquía de importancia, construcción de fundamentos, niveles de madurez.
**Ejemplo:** Maslow del cliente, niveles de madurez en RevOps, jerarquía de necesidades del comprador.
**Forma:** Triángulo dividido en niveles horizontales, base = fundamento, cima = aspiración.

### 13. Mapa de Calor / Tabla de Intensidad
**Cuándo:** Mostrar dónde hay concentración, frecuencia o intensidad de algo.
**Ejemplo:** Qué canales generan más pipeline por segmento, cobertura de contenido por etapa del funnel.
**Forma:** Tabla con filas y columnas, celdas coloreadas por intensidad usando opacidades del color acento.

---

## Estructura del output

Siempre entrega el visual como **HTML autocontenido** (un solo archivo `.html`).

**Todo diagrama debe incluir obligatoriamente:**
- Barra de exportación flotante con botones **Export PNG** y **Export SVG**
- El contenido del diagrama envuelto en `<div id="diagram-export">...</div>`
- Las librerías `html2canvas` y `dom-to-svg` cargadas desde CDN

El HTML debe:
- Tener `<!DOCTYPE html>` completo
- Importar Poppins desde Google Fonts
- Usar las variables CSS de la paleta elegida en `:root`
- Ser responsive (funcionar en 1200px de ancho mínimo)
- Tener fondo del color `--bg` de la paleta
- Ser visualmente limpio — sin sombras excesivas, sin gradientes innecesarios

### Template base HTML (con exportación obligatoria):

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>[Nombre del diagrama]</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
  <style>
    :root {
      --bg: #0A1A3C;
      --card: #10234D;
      --card-alt: #16284F;
      --accent: #E0218A;
      --border: #2A3F6E;
      --text-sec: #9FB0D4;
      --text-faint: #5E6F94;
      --title: #FFFFFF;
      --accent-lt: #FBD0E6;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: var(--bg);
      color: var(--title);
      min-height: 100vh;
      padding: 48px 32px 64px;
    }

    /* ── Export toolbar ── */
    .export-bar {
      position: fixed;
      bottom: 24px;
      right: 24px;
      display: flex;
      gap: 8px;
      z-index: 1000;
    }
    .export-btn {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 8px 16px;
      border: none;
      border-radius: 8px;
      font-family: 'Poppins', sans-serif;
      font-size: 12px;
      font-weight: 600;
      cursor: pointer;
      transition: opacity 0.2s;
    }
    .export-btn:hover { opacity: 0.85; }
    .btn-png {
      background: var(--accent);
      color: #fff;
    }
    .btn-svg {
      background: var(--card);
      color: var(--title);
      border: 1px solid var(--border);
    }
    .export-btn .icon { font-size: 14px; }

    /* ── Estilos específicos del diagrama ── */
    /* ... */
  </style>
</head>
<body>

  <!-- Barra de exportación (siempre presente) -->
  <div class="export-bar">
    <button class="export-btn btn-svg" onclick="exportSVG()">
      <span class="icon">⬡</span> Export SVG
    </button>
    <button class="export-btn btn-png" onclick="exportPNG()">
      <span class="icon">↓</span> Export PNG
    </button>
  </div>

  <!-- Todo el contenido del diagrama va dentro de este div -->
  <div id="diagram-export">

    <!-- Logo top-left -->
    <div class="top-logo">
      <img src="../../branding/rocket-revenue-logo.png" alt="Rocket Revenue">
    </div>

    <!-- contenido del diagrama -->

  </div><!-- /diagram-export -->

  <script>
    // ── Export PNG ──
    function exportPNG() {
      const el = document.getElementById('diagram-export');
      html2canvas(el, {
        backgroundColor: getComputedStyle(document.documentElement)
          .getPropertyValue('--bg').trim() || '#0A1A3C',
        scale: 2,
        useCORS: true,
        logging: false
      }).then(canvas => {
        const link = document.createElement('a');
        link.download = '[nombre-diagrama].png';
        link.href = canvas.toDataURL('image/png');
        link.click();
      });
    }

    // ── Export SVG ──
    function exportSVG() {
      const el = document.getElementById('diagram-export');
      const rect = el.getBoundingClientRect();
      const w = rect.width;
      const h = rect.height;

      // Serializar el HTML como foreignObject dentro de SVG
      const html = el.outerHTML;
      const svgContent = `<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg"
     xmlns:xhtml="http://www.w3.org/1999/xhtml"
     width="${w}" height="${h}" viewBox="0 0 ${w} ${h}">
  <rect width="100%" height="100%" fill="#0A1A3C"/>
  <foreignObject width="${w}" height="${h}">
    <xhtml:div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
      </style>
      ${html}
    </xhtml:div>
  </foreignObject>
</svg>`;

      const blob = new Blob([svgContent], { type: 'image/svg+xml' });
      const url = URL.createObjectURL(blob);
      const link = document.createElement('a');
      link.download = '[nombre-diagrama].svg';
      link.href = url;
      link.click();
      URL.revokeObjectURL(url);
    }
  </script>

</body>
</html>
```

**Nota sobre los nombres de archivo de exportación:** reemplaza `[nombre-diagrama]` en el JS con el nombre real del diagrama usando kebab-case. Ejemplo: `icp-tree`, `funnel-revenue`, `swimlane-handoff`.

### Regla de exportación:
- **PNG** → usa html2canvas a escala 2x (alta resolución). Captura exactamente lo que se ve en el browser.
- **SVG** → envuelve el HTML en `<foreignObject>` dentro de un SVG. Compatible con Figma, Illustrator y navegadores modernos. Para edición vectorial pura, el diseñador deberá re-trazar en Figma usando el SVG como referencia.

---

## Reglas de diseño

1. **Fondo siempre oscuro** — usar `--bg` de la paleta elegida.
2. **Acento con intención** — el color de acento (`--accent`) solo en elementos clave: títulos destacados, números, CTAs, bordes de énfasis.
3. **Texto legible** — títulos en `--title` (#FFFFFF), texto secundario en `--text-sec`.
4. **Bordes sutiles** — usar `--border` con `1px solid` o `border-left` para separar secciones.
5. **Poppins siempre** — no mezclar con otras fuentes.
6. **Sin imágenes externas** — todo geométrico, tipográfico o con íconos Unicode/emoji si aplica.
7. **Espacio generoso** — padding mínimo de 24px en tarjetas, 48px en el contenedor principal.
8. **Números grandes** — cuando el diagrama tiene pasos numerados, el número debe ser grande (60-80px) y en color acento.
9. **Máximo 7 elementos** por diagrama — si hay más, dividir en dos visuales.
10. **Siempre mobile-legible** — aunque el formato principal sea desktop.

---

## Cómo invocar este skill

Ejemplos de solicitudes válidas:

- `/diagrams funnel leads → MQL → SQL → cliente, paleta Azul Eléctrico`
- `/diagrams pipeline horizontal del proceso de onboarding en 6 etapas`
- `/diagrams journey map del cliente B2B desde descubrimiento hasta adopción`
- `/diagrams mapa de relaciones RevOps: Marketing, Ventas, CS y CRM`
- `/diagrams comparativa Inbound vs Outbound vs ABM en 5 dimensiones`
- `/diagrams árbol del ICP: industrias → segmentos → arquetipos`
- `/diagrams flywheel de referidos con 4 etapas, paleta Morado Profundo`
- `/diagrams matriz 2x2 impacto vs esfuerzo de iniciativas comerciales`
- `/diagrams roadmap de implementación RevOps en 3 fases`
- `/diagrams iceberg de por qué se pierden deals`
- `/diagrams swimlane handoff Marketing → Ventas → CS`
- `/diagrams pirámide de madurez RevOps en 5 niveles`
- `/diagrams mapa de calor cobertura de contenido por canal y etapa del funnel`

Si no se especifica paleta, usar **Paleta 1 · Navy + Magenta** por defecto.

---

## Output esperado

1. Archivo HTML listo para abrir en browser.
2. Instrucciones para exportar a PNG si se necesita (screenshot o herramienta de captura).
3. Nota breve: paleta usada, tipo de visual, tamaño recomendado para exportar.
4. Si aplica: sugerencia de dónde usar el visual (LinkedIn, presentación, Notion, email).
