# Rocket Revenue Marketing Agente

Plugin de Claude Code con un equipo completo de agentes especialistas para producir campañas de marketing B2B de alta calidad.

## ¿Qué hace?

Orquesta un equipo de agentes que trabajan en cadena — desde la investigación de mercado hasta la producción visual — para generar contenido alineado al sistema comercial de Rocket Revenue.

## Instalación

```bash
claude --plugin-dir https://github.com/rocket-revenue-latam/rocket-marketing-agente
```

O agregarlo como marketplace dentro de Claude Code:

```
/plugin marketplace add rocket-revenue-latam/rocket-marketing-agente
/plugin install rocket-marketing
```

## Requisitos

- Claude Code con acceso a agentes (`Agent` tool habilitado)
- Skill `/ckm-banner-design` instalado para producción visual de marca
- `OPENAI_API_KEY` en el entorno para generación de imágenes con DALL-E 3
- MCP de Google Drive y Notion configurados para guardar entregables (opcional)

### Configurar OpenAI API Key

Agrega tu key en `~/.claude/settings.json`:

```json
{
  "env": {
    "OPENAI_API_KEY": "tu-key-aqui"
  }
}
```

---

## Agentes disponibles (13)

| Agente | Rol |
|--------|-----|
| `marketing-boss` | Orquestador principal. Coordina las 4 fases de producción. |
| `marketing-research` | Investigación de audiencia, dolores, objeciones y ángulos de contenido. |
| `content-strategist` | Big idea, pilares de contenido y calendario editorial. |
| `SEO-AEO-specialist` | Keywords, preguntas, estructura para buscadores e IA. |
| `copywriter` | Posts, emails, ads, landing pages, carruseles y newsletters. |
| `ads-manager` | Estructura de campañas Meta Ads, LinkedIn Ads y Google Ads. |
| `video-shorts` | Guiones para Reels, Shorts, LinkedIn video y video ads. |
| `repurposing` | Derivados de cada pieza madre para todos los canales. |
| `visual-director` | Briefs visuales para diseñadores y herramientas de diseño. |
| `graphic-producer` | Producción gráfica. Elige automáticamente entre `/ckm-banner-design` y DALL-E 3 según el tipo de pieza. |
| `viz-diagrams` | Diagramas SVG/HTML para frameworks, funnels, journeys y procesos. 14 tipos disponibles, 5 paletas de marca. |
| `video-producer` | Producción de videos a partir de guiones. |
| `qa-brand` | Revisión de calidad y voz de marca antes de publicar. |

---

## Skills disponibles (10)

| Skill | Comando | Descripción |
|-------|---------|-------------|
| Campaign Plan | `/rocket-marketing:campaign-plan` | Plan completo de campaña B2B |
| LinkedIn Post | `/rocket-marketing:linkedin-post` | Posts con tono consultivo B2B |
| Blog SEO/AEO | `/rocket-marketing:blog-seo` | Artículos optimizados para buscadores e IA |
| Newsletter | `/rocket-marketing:newsletter` | Newsletters para audiencias B2B |
| Meta Ads | `/rocket-marketing:meta-ads` | Copies y estructura para Meta Ads |
| Email Sequence | `/rocket-marketing:email-sequence` | Secuencias de email nurturing |
| QA Brand | `/rocket-marketing:qa-brand` | Revisión de calidad y voz de marca |
| Diagrams | `/rocket-marketing:diagrams` | Visuales SVG/HTML con identidad de marca |
| Video Short | `/rocket-marketing:video-short` | Guiones para videos cortos |
| OpenAI Images | `/rocket-marketing:openai-images` | Generación de imágenes con DALL-E 3 |

---

## Flujo de producción

```
Fase 1 — Estrategia
marketing-research → content-strategist → SEO-AEO-specialist

Fase 2 — Contenido
copywriter → video-shorts → ads-manager → repurposing

Fase 3 — Visual
visual-director → briefs
  ├── graphic-producer → /ckm-banner-design (piezas de marca con tipografía y layout exacto)
  │                   → /openai-images DALL-E 3 (imágenes fotorrealistas o conceptuales)
  ├── viz-diagrams    → SVG/HTML (frameworks, funnels, journeys, matrices)
  └── video-producer  → videos a partir de guiones

Fase 4 — Revisión
qa-brand
```

### ¿Cuándo usa cada herramienta de imagen?

`graphic-producer` decide automáticamente según el brief:

| Tipo de pieza | Herramienta |
|---|---|
| Carrusel, banner con texto, pieza de marca | `/ckm-banner-design` |
| Imagen fotorrealista, fondo visual, concepto abstracto | DALL-E 3 (`/openai-images`) |

---

## Uso

Activa el orquestador y dale un objetivo de campaña:

```
Usa el agente marketing-boss para crear una campaña de preventa 
para [producto] dirigida a [audiencia].
```

O invoca skills directamente:

```
/rocket-marketing:campaign-plan campaña de lanzamiento VendeX Q3
/rocket-marketing:linkedin-post sobre los errores más comunes en pipeline B2B
/rocket-marketing:openai-images banner de awareness para Meta Ads, estilo oscuro, concepto de sistema comercial
```

---

## Contexto de marca

Rocket Revenue ayuda a empresas B2B de servicios, tecnología, SaaS, consultoría y servicios profesionales a profesionalizar su sistema comercial para generar más demanda, cerrar más oportunidades y mejorar retención y expansión.

**Paleta:** Navy `#1A2340` · Blanco `#FFFFFF` · Amber `#F59E0B`

**Tono:** consultivo, directo, cercano, profesional. Sin hype. Sin frases genéricas de agencia.
