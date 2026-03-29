---
name: build-landing
description: Construye o actualiza el HTML/CSS completo de la landing page de ClickAngles. Usa cuando quieras generar el archivo index.html con todas las secciones, actualizar el diseño, o añadir una sección nueva al HTML existente.
argument-hint: [all | seccion a agregar/actualizar | fix: descripcion del problema]
auto-activate: false
---

# Build Landing — Constructor de Landing Page ClickAngles

Eres un experto en frontend y landing pages de alta conversión. Tu trabajo es construir HTML/CSS semántico, moderno y optimizado para conversión.

## La tarea es: $ARGUMENTS

Si el argumento es `all`, construye la landing completa desde cero.
Si es el nombre de una sección, agrégala o actualízala en el HTML existente.
Si empieza con `fix:`, corrige el problema descrito.

## Stack técnico

- **HTML5** semántico
- **CSS3** puro con variables CSS (no frameworks externos salvo los listados)
- **Tailwind CDN** permitido si mejora velocidad de desarrollo
- **Google Fonts:** Inter (UI) — cargar via `<link>`
- **Sin JS frameworks** — vanilla JS para interacciones básicas
- **Sin dependencias de build** — debe funcionar abriendo index.html directamente

## Sistema de diseño de ClickAngles

```css
--bg-primary: #0A0A0A;
--bg-secondary: #111111;
--bg-card: #161616;
--border: #222222;
--accent: #DC2626;
--accent-hover: #EF4444;
--success: #10B981;
--warning: #F59E0B;
--text-primary: #F5F5F5;
--text-secondary: #A3A3A3;
--text-muted: #525252;
--font-ui: 'Inter', sans-serif;
```

## Estética

- Fondo negro puro `#0A0A0A`
- Cards con glassmorphism sutil: `background: rgba(255,255,255,0.03); backdrop-filter: blur(10px)`
- Bordes finos: `border: 1px solid #222222`
- Gradientes en acentos: `background: linear-gradient(135deg, #DC2626, #EF4444)`
- Hover states suaves con `transition: all 0.2s ease`
- Sombras oscuras: `box-shadow: 0 4px 24px rgba(0,0,0,0.4)`

## Secciones a incluir (en orden)

1. `<nav>` — Logo + CTA en navbar fija
2. `#hero` — Headline + subheadline + CTA + visual/mockup
3. `#problema` — Pain section
4. `#solucion` — Propuesta de valor
5. `#features` — Grid de módulos con iconos SVG inline
6. `#workflow` — 5 pasos numerados
7. `#social-proof` — Testimonios + métricas
8. `#pricing` — Card de pricing con CTA
9. `#faq` — Accordion de preguntas
10. `#cta-final` — Cierre con CTA
11. `<footer>` — Links mínimos

## Reglas críticas de implementación

1. **Mobile-first** — breakpoints: 375px, 768px, 1280px
2. **CTA buttons** siempre en `--accent` con hover a `--accent-hover`
3. **Secciones alternas** — alternar `--bg-primary` y `--bg-secondary` para separación visual
4. **Smooth scroll** — `html { scroll-behavior: smooth }`
5. **Meta tags** — incluir og:title, og:description, og:image placeholders
6. **Sin imágenes externas** — usar placeholders con `background: --bg-card` y texto descriptivo
7. **Accesibilidad básica** — `alt` en imágenes, `aria-label` en botones sin texto
8. **El archivo de salida es `index.html`** en la raíz del proyecto
