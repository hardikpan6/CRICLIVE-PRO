---
name: Pitchside Precision
colors:
  surface: '#10131a'
  surface-dim: '#10131a'
  surface-bright: '#363940'
  surface-container-lowest: '#0b0e14'
  surface-container-low: '#191c22'
  surface-container: '#1d2026'
  surface-container-high: '#272a31'
  surface-container-highest: '#32353c'
  on-surface: '#e1e2eb'
  on-surface-variant: '#c2c6d3'
  inverse-surface: '#e1e2eb'
  inverse-on-surface: '#2e3037'
  outline: '#8c919c'
  outline-variant: '#424751'
  surface-tint: '#a6c8ff'
  primary: '#a6c8ff'
  on-primary: '#003060'
  primary-container: '#00529b'
  on-primary-container: '#a5c7ff'
  inverse-primary: '#1d5fa8'
  secondary: '#ffecbf'
  on-secondary: '#3d2f00'
  secondary-container: '#fecc00'
  on-secondary-container: '#6e5700'
  tertiary: '#71dc8a'
  on-tertiary: '#003916'
  tertiary-container: '#005f2a'
  on-tertiary-container: '#70db89'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#d5e3ff'
  primary-fixed-dim: '#a6c8ff'
  on-primary-fixed: '#001c3b'
  on-primary-fixed-variant: '#004787'
  secondary-fixed: '#ffe089'
  secondary-fixed-dim: '#f0c100'
  on-secondary-fixed: '#241a00'
  on-secondary-fixed-variant: '#574500'
  tertiary-fixed: '#8ef9a4'
  tertiary-fixed-dim: '#71dc8a'
  on-tertiary-fixed: '#00210a'
  on-tertiary-fixed-variant: '#005324'
  background: '#10131a'
  on-background: '#e1e2eb'
  surface-variant: '#32353c'
typography:
  score-display:
    fontFamily: Montserrat
    fontSize: 48px
    fontWeight: '800'
    lineHeight: '1'
    letterSpacing: -0.04em
  score-display-mobile:
    fontFamily: Montserrat
    fontSize: 36px
    fontWeight: '800'
    lineHeight: '1'
  headline-lg:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
  headline-md:
    fontFamily: Montserrat
    fontSize: 20px
    fontWeight: '700'
    lineHeight: 28px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.08em
  data-mono:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: -0.01em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 16px
  margin-mobile: 16px
  margin-desktop: 32px
  container-max-width: 1280px
---

## Brand & Style
The design system is engineered for a premium, high-stakes sports broadcasting environment. It targets a passionate, data-driven audience that demands real-time accuracy and professional-grade aesthetics. The visual direction is **Glassmorphism mixed with High-Contrast/Bold** elements to create a sense of depth and technical sophistication.

The UI should evoke an "inner-sanctum" feel—authoritative, immersive, and energetic. Every element must feel like part of a live broadcast suite, utilizing semi-transparent layers, vibrant neon-adjacent accents, and crisp typography to maintain legibility during high-velocity play.

## Colors
This design system utilizes a deep-space foundation to allow team colors and live indicators to pop.
- **Base:** The background is a Deep Navy/Black (#0B0E14).
- **Accents:** India Blue (#00529B) serves as the primary action color, while Australia Gold (#FFCD00) and Green (#00843D) are used for team-specific contexts and success states.
- **Live State:** Live Red (#FF0000) is reserved exclusively for real-time indicators and "Out" events, often accompanied by a subtle outer glow.
- **Glass Surfaces:** Use semi-transparent whites for containers to create the glassmorphism effect against the dark base.

## Typography
The typography system prioritizes immediate data recognition. 
- **Montserrat** is used for impactful headlines and large score displays to provide a bold, geometric authority. 
- **Inter** handles all technical data, statistics, and body copy for its exceptional legibility at small sizes and high-density tables.
- **Score Display:** Use the `score-display` role for main innings totals. On mobile, scale this down while maintaining the extra-bold weight to preserve visual impact.
- **Data Mono:** While using Inter, ensure tabular figures (monospaced numbers) are enabled for scorecard alignment.

## Layout & Spacing
The layout follows a **Fluid Grid** model with high-density spacing to accommodate large amounts of statistical data.
- **Grid:** Use a 12-column grid for desktop and a 4-column grid for mobile.
- **Rhythm:** A 4px baseline shift ensures all components—from player stats to over-by-over timelines—align vertically.
- **Mobile-First Navigation:** Primary navigation is anchored to the bottom on mobile (thumb-zone), transitioning to a sticky top-header on desktop.
- **Content Reflow:** On mobile, side-by-side statistics tables should transition to horizontally scrollable cards to prevent data truncation.

## Elevation & Depth
Depth is communicated through **Glassmorphism and Glows** rather than traditional shadows.
- **Layer 0 (Base):** Solid #0B0E14.
- **Layer 1 (Cards):** Surface color `rgba(255, 255, 255, 0.05)` with a `backdrop-filter: blur(12px)` and a 1px border of `rgba(255, 255, 255, 0.12)`.
- **Layer 2 (Overlays/Modals):** Same as Layer 1 but with a subtle `box-shadow: 0 20px 40px rgba(0,0,0,0.4)`.
- **Accents Glow:** Active elements (like the "Live" badge) should use a `drop-shadow` that matches the accent color (e.g., a 4px Red blur) to simulate a broadcast monitor glow.

## Shapes
The design system uses a **Rounded** shape language to soften the technical data and create a premium, modern app feel.
- **Standard Cards:** 16px (rounded-lg) corner radius.
- **Interactive Elements:** Buttons and input fields use 8px (rounded-md) to maintain a professional edge.
- **Timeline Indicators:** Small circular pips for balls in an over, with "6s" and "4s" using the standard 8px rounding.
- **Avatars:** Circular (pill) masks for player profile photos.

## Components
- **Sticky Score Header:** A persistent bar showing the current score, run rate, and batsman. It uses a high-blur glass effect to allow content to scroll underneath while remaining legible.
- **Live Badge:** A small capsule with a pulsating Live Red dot and white text. 
- **Statistics Tables:** Use zebra-striping with `rgba(255, 255, 255, 0.02)` for alternate rows. Headers should use the `label-caps` typography style.
- **Timeline Indicator:** A horizontal scrolling component showing the last 12-24 balls. Each ball is a 32x32px glass square; color-coded borders denote runs (Gold), wickets (Red), or dots (White).
- **Primary Buttons:** Solid India Blue (#00529B) with white Montserrat text. Use a subtle inner-glow on hover.
- **Input Fields:** Darker than the card background, using a 1px Gold border only when focused to indicate active data entry.
- **Player Cards:** Feature a background gradient that blends from the team color (e.g., India Blue) into the glass base.