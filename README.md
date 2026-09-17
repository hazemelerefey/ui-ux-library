# 🎨 UI/UX Library

A shared, growing library of fonts, icons, design styles, assets, and AI workflows — built to power every project we create together.

> **Workflow rule:** Every project we work on → we collect materials → push here → build the project using library assets → library grows permanently for future use.

---

## 📂 Folder Structure

```
ui-ux-library/
├── fonts/
│   ├── google-fonts/      ← Fonts available on Google Fonts (free, web-native)
│   ├── self-hosted/       ← Fonts requiring self-hosting (free/commercial licensed)
│   └── variable/          ← Variable font files (.woff2 preferred)
│
├── icons/
│   ├── phosphor/          ← Phosphor icon sets (MIT)
│   ├── lucide/            ← Lucide icons (MIT)
│   └── custom/            ← Custom SVG icons created for specific projects
│
├── styles/
│   ├── guidelines/        ← Design philosophy, trend guides, design system rules
│   └── tokens/            ← Color palettes, spacing scales, radius tokens
│
├── assets/
│   ├── images/            ← Reusable background textures, gradients, stock imagery
│   ├── 3d-models/         ← Spline / Three.js compatible 3D assets
│   └── videos/            ← Motion assets, Higgsfield exports, background loops
│
├── skills/
│   ├── design/            ← AI design skills, Penpot workflows, ideation guides
│   ├── development/       ← Frontend dev skills, Next.js patterns, GSAP guides
│   └── workflow/          ← Project workflow docs, brainstorming templates
│
└── projects/
    └── youssef-sherif-portfolio/   ← Project-specific notes, decisions, assets
```

---

## 🚀 Projects Using This Library

| Project | Status | Key Assets Used |
|---|---|---|
| Youssef Sherif Portfolio | 🔄 In Progress | fonts, icons, 2026-style-guide |

---

## ⚡ Quick Principles

- **One icon library per project** — don't mix Phosphor with Lucide in the same UI
- **Variable fonts preferred** — single file, full weight range, smaller bundle
- **Always check license** — columns: Free (personal) / Commercial OK / Attribution required
- **Animate `transform` & `opacity` only** — GPU composited, no layout thrash
- **Drive Lenis via `gsap.ticker`** — single RAF loop for buttery scroll performance
