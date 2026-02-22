# ALIGN Intelligence -Design System Guide

Reference specification for all visual materials, presentations, and web properties.

---

## Aesthetic

**McKinsey x Intelligence Agency** -PE-grade institutional. Dark premium. No startup gradients, no playful illustrations. Command center precision meets institutional authority.

---

## Color Palette

### Primary Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#020B1A` | Deep navy -primary background |
| `--surface` | `#071222` | Section background (alternating) |
| `--surface-2` | `#0c1a2e` | Section background (alternating) |
| `--card` | `#0f1f36` | Card backgrounds |
| `--card-hover` | `#142740` | Card hover state |

### Accent Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--gold` | `#C9A050` | Institutional gold -primary accent, CTAs, labels |
| `--gold-lt` | `#dfc477` | Light gold -quotes, highlights |
| `--cyan` | `#00D4FF` | Intelligence/tech -secondary accent, data, Force 3 |
| `--red` | `#FF4B4B` | Alerts, critical flags (use sparingly) |

### Text Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--white` | `#eef0f4` | Headlines, emphasis |
| `--text` | `#d0d5e0` | Primary body text |
| `--text-2` | `#6e82a0` | Secondary text, descriptions |
| `--text-3` | `#3e5270` | Tertiary text, labels, HUD codes |

### Border Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--border` | `rgba(201,160,80,0.18)` | Gold borders (cards, dividers) |
| `--border-cyan` | `rgba(0,212,255,0.14)` | Cyan borders (Force 3, SIGINT) |

---

## Typography

### Font Stack

| Role | Font | Weights | Usage |
|------|------|---------|-------|
| **Headings & Body** | Inter | 300, 400, 500, 600, 700 | All headings, body text |
| **Monospace** | JetBrains Mono | 300, 400, 500, 600 | Labels, HUD codes, tags, numbers |
| **Quotes** | Cormorant Garamond | 300-700, italic | Pull quotes, emphasis |

### Type Scale (Presentation Grade)

| Class | Size | Weight | Style |
|-------|------|--------|-------|
| `.h1` | clamp(38px, 7vw, 74px) | 700 | UPPERCASE, letter-spacing .08em |
| `.h2` | clamp(30px, 5vw, 54px) | 600 | UPPERCASE, letter-spacing .06em |
| `.h3` | 20px | 600 | UPPERCASE, letter-spacing .04em |
| `.label` | 13px | 500 (Mono) | UPPERCASE, letter-spacing 4px, gold |
| `.sub` | clamp(17px, 2vw, 22px) | 400 | Sentence case, max-width 720px |
| `.body` | 16px | 400 | Sentence case |
| `.quote` | clamp(20px, 2.8vw, 32px) | italic (Serif) | Gold, serif |

---

## Layout

### Grid System

| Class | Columns (Mobile) | Columns (Tablet) | Columns (Desktop) |
|-------|-------------------|--------------------|--------------------|
| `.g2` | 1 | 2 | 2 |
| `.g3` | 1 | 2 | 3 |
| `.g4` | 2 | 2 (gap 16px) | 4 |

### Breakpoints

| Name | Width | Padding (--px) | Section Padding (--py) |
|------|-------|----------------|------------------------|
| Mobile | < 768px | 24px | 80px |
| Tablet | 768px+ | 40px | 100px |
| Desktop | 1200px+ | 56px | 120px |

### Sections

- Max-width: `1360px`, centered
- Each section: `min-height: 100vh` (slide-like)
- Alternating backgrounds: `--surface` / `--surface-2`
- Exception: Team section uses `sec--auto` (content-driven height)

---

## Components

### Card

```
Background: var(--card)
Border: 1px solid var(--border)
Border-radius: 2px
Padding: 24px 20px
Top bar: 2px solid var(--gold) or var(--cyan)
Hover: translateY(-2px), border-color gold, subtle box-shadow
```

### HUD Bar

```
Flex row, space-between
Bottom border: 1px solid var(--border)
Left: ALIGN icon (16px, 40% opacity)
Right: Monospace code label (11px, uppercase, text-3)
```

### Pill / Tag

```
Pill: Mono 12px, uppercase, 1px border, gold/cyan
Tag: Mono 11px, uppercase, gold-dim background
```

### Highlight Box

```
Background: linear-gradient gold 5% to 2%
Left border: 2px solid gold
Serif italic text in gold-lt
```

### Timeline

```
Horizontal (desktop) / Vertical (mobile)
2px border line with gold dots
Mono labels + Inter titles
```

### Progress Bar

```
3px track (gold 8% opacity)
Fill: linear-gradient gold to cyan
Animated width on scroll intersection
```

---

## Tactical Patterns

### Grid Overlay

Subtle 60x60px grid using gold at 2.5% opacity with radial fade to transparent.

### Scanline

1px height, cyan at 12% opacity, horizontal gradient, 8s infinite animation.

### Background Images

Diagrams and renders placed as absolute-positioned layers at 6-7% opacity.

---

## Color Assignment Rules

| Element | Color |
|---------|-------|
| Force 1 (TFT) | Gold |
| Force 2 (Corridor X) | Cyan |
| Force 3 (Intelligence) | Cyan |
| HUMINT | Gold |
| SIGINT | Cyan |
| Founders & ESI team | Gold borders |
| Intelligence & Corridor X team | Cyan borders |
| Labels, CTAs, primary accents | Gold |
| Data, tech, intelligence accents | Cyan |

---

## Asset Conventions

- Icons: SVG, line-art style, 36x36px display
- Diagrams: PNG renders or inline SVG
- Backgrounds: PNG, used at 6% opacity as overlays
- Headshots: JPEG/PNG, displayed in 48x48 circular frames
- Partner logos: SVG preferred, grayscale filter with brightness boost

### File Naming

```
assets/
  backgrounds/     hero-grid.png, section-pattern.png
  diagrams/        organism-render.png, cortex-diagram.svg
  icons/           icon-brain.svg, icon-shield.svg
  logos/            align-logo.svg, align-icon.svg
  logos/partners/   sp-global.svg, cisco.svg
  headshots/        dror-barak.jpg, silhouette-gold-m.png
  photos/           cta-visual.png
```
