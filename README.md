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
```

## Agentes disponibles

| Agente | Rol |
|--------|-----|
| `marketing-boss` | Orquestador principal. Coordina todas las fases de producción. |
| `marketing-research` | Investigación de audiencia, dolores, objeciones y ángulos de contenido. |
| `content-strategist` | Big idea, pilares de contenido y calendario editorial. |
| `SEO-AEO-specialist` | Keywords, preguntas, estructura para buscadores e IA. |
| `copywriter` | Posts, emails, ads, landing pages, carruseles y newsletters. |
| `ads-manager` | Estructura de campañas Meta Ads, LinkedIn Ads y Google Ads. |
| `video-shorts` | Guiones para Reels, Shorts, LinkedIn video y video ads. |
| `repurposing` | Derivados de cada pieza madre para todos los canales. |
| `visual-director` | Briefs visuales para diseñadores y herramientas de diseño. |
| `graphic-producer` | Producción de piezas gráficas usando `/ckm-banner-design`. |
| `video-producer` | Producción de videos a partir de guiones. |
| `qa-brand` | Revisión de calidad antes de publicar. |

## Skills disponibles

| Skill | Descripción |
|-------|-------------|
| `/rocket-marketing:campaign-plan` | Plan completo de campaña B2B |
| `/rocket-marketing:linkedin-post` | Posts para LinkedIn con tono consultivo B2B |
| `/rocket-marketing:blog-seo` | Artículos optimizados para SEO y AEO |
| `/rocket-marketing:newsletter` | Newsletters para audiencias B2B |
| `/rocket-marketing:meta-ads` | Copies y estructura para Meta Ads |
| `/rocket-marketing:email-sequence` | Secuencias de email nurturing |
| `/rocket-marketing:qa-brand` | Revisión de calidad y voz de marca |
| `/rocket-marketing:diagrams` | Diagramas y visuales SVG/HTML con identidad Rocket Revenue |
| `/rocket-marketing:video-short` | Guiones para videos cortos |

## Flujo de producción

```
Fase 1 — Estrategia
marketing-research → content-strategist → SEO-AEO-specialist

Fase 2 — Contenido
copywriter → video-shorts → ads-manager → repurposing

Fase 3 — Visual
visual-director → graphic-producer (/ckm-banner-design) → video-producer

Fase 4 — Revisión
qa-brand
```

## Uso

Activa el orquestador principal y dale un objetivo de campaña:

```
Usa el agente marketing-boss para crear una campaña de preventa para [producto] dirigida a [audiencia].
```

## Contexto de marca

Rocket Revenue ayuda a empresas B2B de servicios, tecnología, SaaS, consultoría y servicios profesionales a profesionalizar su sistema comercial para generar más demanda, cerrar más oportunidades y mejorar retención y expansión.

**Tono:** consultivo, directo, cercano, profesional. Sin hype. Sin frases genéricas de agencia.

## Requisitos

- Claude Code con acceso a agentes (`Agent` tool habilitado)
- Skill `/ckm-banner-design` instalado para producción visual
- MCP de Google Drive y Notion configurados para guardar entregables (opcional)
