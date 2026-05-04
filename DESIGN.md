---
name: contractor-template
description: Premium single-page website template for US trades contractors — plumber, HVAC, electrician, builder. Designed to showcase Minter workflow quality.
brand:
  primary: "#1B2B3A"
  secondary: "#2D4A5E"
  accent: "#C8963E"
  background: "#F7F5F2"
  surface: "#FFFFFF"
  surfaceAlt: "#F0EDE8"
  text: "#1A1A1A"
  textMuted: "#6B7280"
  border: "#E5E0D8"
  success: "#2D7D46"
  error: "#C0392B"
typography:
  heading: "Syne, weight 700"
  body: "DM Sans, weight 400"
  mono: "DM Mono, weight 400"
spacing:
  unit: 8
  scale: "4 8 12 16 24 32 48 64 96 128"
components:
  card: "{ bg: white, border: 1px solid #E5E0D8, radius: 16px, shadow: none }"
  button: "{ padding: 14px 28px, radius: 9999px, fontWeight: 600 }"
  input: "{ border: 1.5px solid #E5E0D8, focusRing: #C8963E, radius: 12px }"
---

# Contractor Template — Design Specification

## 1. Overview

Single-page premium website template for US trades contractors (plumber, HVAC, electrician, builder). Positioned as a demonstration of quality — warm, confident, trustworthy. Designed to convert US homeowners and light commercial clients who are evaluating the quality of the work.

**One memorable thing:** The hero text "We Show Up" — a direct promise that addresses the #1 frustration customers have with trades businesses.

## 2. Design Language

### Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-primary` | #1B2B3A | Headlines, nav, CTAs |
| `--color-secondary` | #2D4A5E | Sub-headings, secondary text |
| `--color-accent` | #C8963E | Accent: stars, underlines, CTA hover, badges |
| `--color-bg` | #F7F5F2 | Page background (warm off-white) |
| `--color-surface` | #FFFFFF | Cards, nav |
| `--color-surface-alt` | #F0EDE8 | Section dividers, alternate sections |
| `--color-text` | #1A1A1A | Body text |
| `--color-text-muted` | #6B7280 | Captions, labels |
| `--color-border` | #E5E0D8 | Card borders, dividers |
| `--color-success` | #2D7D46 | Success states, checkmarks |

### Typography

- **Display / H1:** Syne 700, 56–80px, tracking -0.03em, line-height 1.05
- **H2:** Syne 700, 36–48px, tracking -0.02em, line-height 1.15
- **H3:** Syne 600, 22–26px, tracking -0.01em, line-height 1.3
- **Body:** DM Sans 400, 16–18px, line-height 1.7, max-width 65ch
- **Labels / Caps:** DM Sans 500, 12–13px, tracking 0.08em, UPPERCASE
- **Never:** Inter, Roboto, Arial, Poppins, Open Sans

### Spatial System

8pt grid. Major section padding: 96px top/bottom (desktop), 64px (tablet), 48px (mobile).

### Motion

- Page load: hero text reveal with stagger (opacity 0→1, translateY 24px→0, 500ms ease-out, 80ms stagger)
- Scroll reveal: sections animate in at 15% viewport intersection (opacity + translateY, 400ms ease-out)
- Hover: buttons scale(1.02), shadow lift, 200ms ease
- Nav: background transitions from transparent to white + shadow at scroll > 60px
- All motion: `prefers-reduced-motion` respected

### Visual Assets

- Icons: Inline SVG (custom, minimal line style, 1.5px stroke)
- Images: Unsplash / picsum via URL (trades: tools, work, professional)
- Decorative: Thin amber rule lines, large outline numbers, geometric grid patterns

## 3. Layout & Structure

```
[Sticky Nav]
[Hero — asymmetric split: text left, image right]
[Trust Bar — 4 credentials in a row]
[Services — 2x2 grid with icon, title, description]
[About / Why Us — offset 2-col: image left, text right]
[Testimonials — 3-card carousel]
[Metrics Band — 3 bold stats]
[CTA — full-width dark section: headline + form]
[Footer — 3-col: brand, services, contact]
```

**Responsive:** Mobile-first. Single column on <768px. Two-column on 768–1024px. Full layout on 1024px+.

## 4. Components

### Navigation
- Logo: text-based "CRAFTLINE" in Syne bold
- Links: Services, About, Reviews (smooth scroll)
- CTA: amber pill button "Get Free Estimate"
- Sticky: transparent → white + shadow on scroll

### Hero
- Left: eyebrow label, H1 "We Show Up.\nOn Time. Every Time.", subtext, 2 CTA buttons
- Right: full-bleed image with amber diagonal overlay accent
- Mobile: stacked, image first (before text)

### Trust Bar
- 4 items: Years in Business | Jobs Completed | 5-Star Reviews | Licensed & Insured
- Dividers between items, amber accent on numbers

### Services Card
- Icon (inline SVG), H3 title, body text, "Learn more →" link
- Hover: card lifts with shadow, amber left-border accent appears
- 2×2 grid desktop, 1-col mobile

### About Section
- Left: image with amber geometric frame overlay
- Right: H2 "Built Different.", 3 bullet benefits with amber checkmarks, CTA

### Testimonial Card
- Large quote mark (amber), testimonial text, star rating, name + city
- 3 cards side-by-side desktop, carousel on mobile

### Metrics Band
- Dark navy background, 3 large stats with amber accent numbers
- "Projects Completed" | "Years of Experience" | "5-Star Reviews"

### CTA Section
- Dark navy background, H2, subtext, 2 inputs (name + phone) + submit button
- Amber CTA button, success/error states on submit

### Footer
- 3 columns: Brand | Services | Contact
- Phone, email, service area cities, copyright

## 5. Named Design Rules

1. **Amber Accent Only:** Gold/amber (#C8963E) used ONLY for: star ratings, numbered stats, CTA buttons and hovers, decorative rule lines, service card left-border on hover
2. **Warm Surface Hierarchy:** Background #F7F5F2, Cards #FFFFFF — never reverse this
3. **No Shadow at Rest:** Cards are flat at rest. Shadow only on hover.
4. **No Centered Hero:** Hero text is always left-aligned; image anchors right
5. **No Purple/Blue Gradients:** The entire palette is warm — navy + amber + warm neutrals

## 6. Technical

- Single `index.html` — no build step
- CSS custom properties in `:root`
- Vanilla JS — scroll animations, form handler, nav scroll behavior
- Fonts: Google Fonts (Syne, DM Sans, DM Mono)
- Images: picsum.photos (reliable, no broken links)
- Form: client-side validation + simulated submission
