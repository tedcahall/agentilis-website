# Agentilis Website

> *agere · ilis* — characterized by action

The official website for **[Agentilis](https://agentilis.ai)** — a business optimization and growth firm powered by agentic AI. Built by AI agents, directed by humans, shipped to the web.

---

## What This Is

This repository contains the complete front-end source for agentilis.ai — every page, every stylesheet, every line of markup. It is a static HTML + CSS + JavaScript site with no build step, no framework, and no dependencies beyond Google Fonts. It loads fast, renders beautifully, and works on every device.

It was designed and built entirely by **Vignelli** — the Agentilis creative and design agent — under the direction of Ted Cahall and with copy written by **Ogilvy**, the Agentilis marketing agent. No human wrote a line of production code. That is the point.

---

## Design System

### Color Palette — *Patina*

| Role | Name | Hex |
|------|------|-----|
| Primary | Dark Slate | `#2C3E4A` |
| Accent | Cool Sage | `#7A9E8E` |
| Background | Warm White | `#FAFAF7` |
| Text | Near Black | `#1F1F1F` |

The palette was developed by Ogilvy under the creative direction *Roman Engineering* — not another AI startup look, but something that feels like permanence, craft, and earned authority. Stone and bronze translated into pixels.

### Typography

| Use | Typeface | Source |
|-----|----------|--------|
| Headlines & Display | [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) | Google Fonts |
| Body, UI & Captions | [Inter](https://fonts.google.com/specimen/Inter) | Google Fonts |

Playfair Display brings Roman letterform roots and editorial weight to every headline. Inter handles the prose and interface with screen-optimized legibility. Together they communicate: *technical authority in the headlines, human clarity in the prose.*

### Layout Principles

- 12-column grid, `max-width: 1160px` container
- 8px base spacing unit — all margins, padding, and gaps are multiples
- White space as a design element, not leftover space
- Responsive at three breakpoints: desktop (full), tablet (≤960px), mobile (≤720px)
- Mobile navigation: hamburger toggle, JS-powered, zero dependencies

---

## Pages

### 🏠 Home — `/`
The entry point. A full-bleed hero with the headline *Characterized by action.*, a proof stats row (40+ years, 4× COO, 9 agents, 24/7), a services teaser with links to the Agentic page, and a closing CTA.

### ⚙️ Services — `/services/`
Seven distinct service offerings, each with a two-paragraph description and an italic *Best for:* line. Rendered in a responsive 2-column card grid. Services range from CEO Advisory to AI-Based Lead Generation.

### 🤖 Agentic — `/agentic/`
A five-section essay making the case for agentic AI over chatbots. This is the intellectual heart of the Agentilis proposition — what the word *agentic* actually means, how it differs from a faster keyboard, and why the ceiling is growth rather than cost reduction. Closes with: *Optimization is the floor. Growth is the ceiling.*

### 👥 Team — `/team/`
The full Agentilis team — human and agent alike. Four human principals in a 4-column desktop grid, followed by 10 AI agents in a 3-column grid across four rows. The agents are named with intention: Max (Chief of Staff), James (after James Gosling), Ken (after Ken Thompson), Watts (after Watts Humphrey), Argus (the all-seeing giant of Greek mythology), Gantt (after Henry Gantt), Ogilvy (after David Ogilvy), Vignelli (after Massimo Vignelli), Guido (after Guido van Rossum), and Dale Inman (after NASCAR's all-time crew chief record holder).

### 👤 Founder — `/founder/`
Ted Cahall's story. Four decades at the intersection of technology and operations — AT&T Bell Labs, CNET, AOL, Microsoft, Digital River, block.one. Named Executive Officer on three public companies. Two US patents. Proof before pitch: marrspoints.com, running for over 15 years continuously, now operated by the Agentilis agent team.

### 📖 Story — `/story/`
Eight chapters on how Agentilis was built — agent by agent, problem by problem, proof point by proof point. It starts with Max scheduling meetings at 5AM and ends with human partners joining a team that was already working. The story of a company that built its own proof of concept before it had its first client.

---

## File Structure

```
agentilis-website/
│
├── index.html              # Home page
├── site.css                # Global stylesheet — all design tokens and components
│
├── services/
│   └── index.html          # Services page — 7 offerings
│
├── agentic/
│   └── index.html          # Agentic essay — chatbots vs. agents
│
├── team/
│   └── index.html          # Team — principals and agent staff
│
├── founder/
│   └── index.html          # Founder — Ted Cahall biography
│
├── story/
│   └── index.html          # Story — 8-chapter origin narrative
│
└── ted-cahall.jpg          # Founder photo
```

---

## Technical Notes

### No Build Step
This is intentional. No Webpack, no Vite, no npm, no node_modules. Every file is exactly what the browser receives. Edit a file, refresh the page. That is the entire workflow.

### CSS Architecture
All styles live in `site.css`. Design tokens are defined as CSS custom properties on `:root` — colors, spacing units, border radii. Components are organized with clearly labeled sections. Responsive overrides live at the bottom in a single `@media` block.

### JavaScript
Minimal and purposeful. One small inline script per page handles the mobile navigation toggle. No libraries. No frameworks. No third-party scripts of any kind.

### Performance
- No render-blocking resources beyond Google Fonts (loaded with `display=swap`)
- No JavaScript on initial render
- Images: single JPEG for the founder photo
- Target: Lighthouse 90+ across all four categories

### Hosting
Production target: **AWS S3 + CloudFront**. Ken (the Agentilis systems administrator agent) handles all deployments. The preview server runs on nuc2 via Apache on port 90, with the document root mapped to this repository's working directory.

---

## The Team That Built This

| Who | Role | What they did here |
|-----|------|--------------------|
| **Ogilvy** | Marketing Agent | Brand strategy, color system, all copy, service definitions |
| **Vignelli** | Creative & Design Agent | Design system, all HTML + CSS, layout, typography, mobile |
| **Ted Cahall** | Founder | Direction, decisions, approvals |

Ogilvy is named after David Ogilvy, the Father of Advertising.
Vignelli is named after Massimo Vignelli, Italian master designer — who designed the NYC subway map, the American Airlines identity, and believed the world needed only about a dozen typefaces.

*"The life of a designer is a life of fight — fight against the ugliness."*
— Massimo Vignelli

---

## Status

| Page | Status |
|------|--------|
| Home | ✅ Live |
| Services | ✅ Live |
| Agentic | ✅ Live |
| Team | ✅ Live |
| Founder | ✅ Live |
| Story | ✅ Live |
| Contact | 🔲 Planned |
| AI Brief / Subscribe | 🔲 Planned |

---

## License

Proprietary. All rights reserved. © 2026 Agentilis.

---

*This README was written by Vignelli.*
