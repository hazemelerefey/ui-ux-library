# Hero Section — Design Spec & Component Architecture

> **Status**: Generated & Approved in Penpot  
> **Board**: `Hero — Architectural Monolith (1920x1080)`  
> **Aesthetic**: Architectural Cinema / Dark Luxury Editorial (Anti-AI-Slop)

---

## 🎨 Design Tokens

### Colors (Hex & Roles)
```css
:root {
  --canvas-bg: #0B0C0E;        /* Deep Obsidian Charcoal */
  --monolith-outer: #121418;   /* Recessed Architectural Niche */
  --monolith-inner: #0D0E11;   /* Bevel Niche Depth */
  --monolith-plate: #15181F;   /* Portrait Stage Plate */
  
  --hairline-border: #1A1D24;  /* Structural Grid Guides */
  --hairline-divider: #1C2027; /* Column Separator */
  --button-border: #2B303A;    /* Secondary Action Border */

  --text-primary: #F4F4F0;     /* Sculptural Bone White */
  --text-secondary: #E2E4E9;   /* Technical Headline Tint */
  --text-muted: #9CA3AF;       /* Body & Narrative Grey */
  --text-subtle: #6B7280;      /* Eyebrow & Telemetry */
  --text-dark: #0B0C0E;        /* Primary Button Text */
}
```

### Typography Roles
* **Display Name**: `YOUSSEF SHERIF` — 120px / 900 Black / Line-height 0.95 / Letter-spacing -0.03
* **Role Masthead**: `MACHINE LEARNING DEVELOPER` — 52px / 700 Bold / Letter-spacing 0.01
* **Narrative Copy**: 16px / 400 Regular / Line-height 1.6 / Max-width 480px
* **Metadata & Eyebrows**: 12px / 600 SemiBold / All-caps / Letter-spacing 0.14
* **Navigation & Triggers**: 12px–13px / 600–700 Bold / Letter-spacing 0.04–0.08

---

## 📐 Layout Geometry (1920x1080)

| Element | Geometry (x, y, w, h) | Styling |
|---|---|---|
| **Top Hairline** | (80, 88, 1760, 1) | Border `#1A1D24` |
| **Bottom Hairline** | (80, 990, 1760, 1) | Border `#1A1D24` |
| **Brand Mark** | (80, 38) | 13px / 700 / `#E5E7EB` |
| **Nav Links** | (820–1135, 40) | 12px / 600 / `#9CA3AF` |
| **Resume CTA** | (1730, 26, 110, 36) | 6px radius / 1px border `#2C313C` |
| **Left Eyebrow** | (80, 170) | 12px / 600 / `#6B7280` |
| **Giant Name** | (80, 210–460) | 120px / 900 / `#F4F4F0` |
| **Role Subhead** | (80, 490–650) | 52px / 700 / `#E2E4E9` |
| **Column Divider** | (80, 670, 880, 1) | Border `#1C2027` |
| **Thesis Statement**| (80, 705–775) | 16px / 400 / `#9CA3AF` |
| **Primary Button** | (80, 800, 210, 48) | 8px radius / Solid `#F4F4F0` |
| **Secondary Button**| (310, 800, 140, 48) | 8px radius / 1px border `#2B303A` |
| **Outer Monolith** | (1080, 120, 760, 830) | 24px radius / Fill `#121418` |
| **Inner Bevel** | (1104, 144, 712, 782) | 18px radius / Fill `#0D0E11` |
| **Portrait Stage** | (1130, 170, 660, 730) | 14px radius / Fill `#15181F` |

---

## 🎬 2026 Motion Choreography (Next.js + GSAP)

1. **Preloader Exit**:
   * Counter ticks `00` ➔ `100%` in bottom-right.
   * On complete, horizontal shutter curtain slides away (`power4.inOut`, 1.1s).
   * Monolith frame recedes into place with 3D camera push.
   * Typographic name splits line-by-line (`y: 40`, `opacity: 0` ➔ `1`, stagger: 0.08s).
2. **Interactive 3D Cursor Parallax**:
   * Mouse position drives subtle `rotateX` / `rotateY` (-3° to +3°) on the portrait stage plate with smooth damping (`gsap.quickTo`).
   * Gives the feeling of looking into a recessed physical architectural alcove.
3. **Scroll Scrub Departure**:
   * As scroll starts, the monolith expands into a panoramic letterbox.
   * Typographic title shrinks into sticky header wordmark.
   * Section 02 (Philosophy & DAFEsteel Work) rises smoothly from below.
