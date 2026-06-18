---
name: BadgePing Mini
colors:
  surface: '#fcf8fa'
  surface-dim: '#dcd9db'
  surface-bright: '#fcf8fa'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f5'
  surface-container: '#f0edef'
  surface-container-high: '#eae7e9'
  surface-container-highest: '#e4e2e4'
  on-surface: '#1b1b1d'
  on-surface-variant: '#45464d'
  inverse-surface: '#303032'
  inverse-on-surface: '#f3f0f2'
  outline: '#76777d'
  outline-variant: '#c6c6cd'
  surface-tint: '#565e74'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#131b2e'
  on-primary-container: '#7c839b'
  inverse-primary: '#bec6e0'
  secondary: '#505f76'
  on-secondary: '#ffffff'
  secondary-container: '#d0e1fb'
  on-secondary-container: '#54647a'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#271901'
  on-tertiary-container: '#98805d'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2fd'
  primary-fixed-dim: '#bec6e0'
  on-primary-fixed: '#131b2e'
  on-primary-fixed-variant: '#3f465c'
  secondary-fixed: '#d3e4fe'
  secondary-fixed-dim: '#b7c8e1'
  on-secondary-fixed: '#0b1c30'
  on-secondary-fixed-variant: '#38485d'
  tertiary-fixed: '#fcdeb5'
  tertiary-fixed-dim: '#dec29a'
  on-tertiary-fixed: '#271901'
  on-tertiary-fixed-variant: '#574425'
  background: '#fcf8fa'
  on-background: '#1b1b1d'
  surface-variant: '#e4e2e4'
typography:
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: 0em
  body-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
    letterSpacing: 0em
  label-caps:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
  mono-data:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 18px
    letterSpacing: -0.02em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  container-padding: 16px
  gap-dense: 8px
  gap-standard: 12px
  bento-margin: 16px
---

## Brand & Style

The design system is centered on high-density utility and professional reliability. It targets technical users who require immediate clarity on system status without visual noise. The personality is "Quiet Authority"—a tool that stays out of the way until it is needed, providing a calm, focused environment for monitoring and debugging.

The aesthetic follows a **Modern Utilitarian** approach, blending elements of "Bento" layouts with industrial precision. It prioritizes information hierarchy through structured containers, subtle depth, and a strict adherence to functional color application. There are no decorative elements; every line, shadow, and color shift serves a specific semantic purpose.

## Colors

This design system utilizes a Neutral Slate palette to ground the interface, ensuring that semantic status colors remain the primary focus of the user's attention.

- **Base & Neutrals:** A Slate scale provides the foundation. `#f8fafc` is used for the application background, while pure `#ffffff` is reserved for elevated containers and "Bento" cells to create clear separation.
- **Semantic Colors:**
    - **Pass (Emerald):** Used for healthy pings, successful requests, and "Up" states.
    - **Warn (Amber):** Used for latency spikes, nearing limits, or transient issues.
    - **Fail (Rose):** Used for timeouts, 500-level errors, and "Down" states.
- **Accents:** The primary color is a deep Midnight Slate (`#0f172a`) used for text and primary interactive affordances to maintain a professional, high-contrast look without the harshness of pure black.

## Typography

The typography system is designed for high-density reading and technical data parsing. 

- **Primary Sans (Inter):** Chosen for its exceptional legibility at small sizes. We use tight letter spacing and a slightly reduced line height compared to marketing sites to allow more data to fit on screen.
- **Technical Mono (JetBrains Mono):** Specifically used for JSON viewers, IP addresses, timestamps, and status codes. This ensures that character alignment is preserved when comparing multiple lines of log data.
- **Information Density:** Use `body-sm` as the standard for most interface text. Use `label-caps` for section headers within Bento cards to provide a clear structural anchor.

## Layout & Spacing

The layout utilizes a **Fixed Bento Grid** philosophy. Content is organized into modular cards with explicit borders.

- **The Grid:** A 12-column grid is used for desktop, but the primary logic is "Row-based modules." Modules should have a standard height where possible to maintain visual alignment.
- **Spacing Rhythm:** Based on a 4px baseline. Most internal paddings should be `12px` (3 units) or `16px` (4 units). Dense data tables or JSON views should drop to `8px` (2 units) to maximize vertical space.
- **Breakpoints:**
    - **Desktop:** Multi-column bento layout.
    - **Mobile:** Single column stack. Margin reduces to `12px` at the screen edges to maximize the utility of the small viewport.

## Elevation & Depth

This design system uses **Tonal Layering** and **Ghost Outlines** rather than heavy shadows to signify depth.

- **Level 0 (Background):** `#f8fafc` — The canvas on which the application sits.
- **Level 1 (Cards/Modules):** White surface with a 1px border of `#e2e8f0`. This is the standard container for pings and metrics.
- **Level 2 (Active/Hover):** A very soft, diffused shadow (`0 4px 6px -1px rgb(0 0 0 / 0.05)`) is applied only when a card is hovered or focused, indicating it can be clicked or expanded.
- **JSON Containers:** Use a slightly inset appearance (Background: `#f1f5f9`) to differentiate code/data areas from the rest of the UI.

## Shapes

The shape language is "Soft-Square." It maintains a professional, systematic feel by avoiding overly circular "bubble" aesthetics.

- **Containers:** Bento cards and main containers use a `0.5rem` (8px) radius.
- **Interactive Elements:** Buttons, inputs, and toggles use a `0.25rem` (4px) radius to feel more precise and technical.
- **Status Indicators:** Small status dots are circular, but status "tags" follow the 4px button radius.

## Components

- **Buttons:** Small and precise. Primary buttons use Slate-900 backgrounds with white text. Secondary buttons are outlined. The height is capped at 32px for a compact feel.
- **Status Chips:** Small badges with a light tinted background and dark text of the same hue (e.g., Emerald-100 bg with Emerald-800 text). Include a 6px solid dot for visual accessibility.
- **Bento Cards:** The core wrapper. Must include a header area with `label-caps` text and an optional "Action" area for icons or toggles.
- **JSON Viewer:** Monospaced text inside a `#f1f5f9` container with subtle syntax highlighting using the semantic color palette (Strings in Slate-600, Keys in Slate-900, Booleans in Pass/Fail colors).
- **Toggles:** Minimalist switch design. When 'Off', it blends with the border color. When 'On', it uses the Primary Slate-900 to avoid confusion with semantic Pass/Fail colors.
- **Inputs:** Clean, 1px bordered boxes with no inner shadow. Focus state is indicated by a 2px Slate-900 ring with an offset.