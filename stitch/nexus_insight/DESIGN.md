# Design System Specification

## 1. Overview & Creative North Star: "The Architectural Authority"
This design system moves beyond the generic SaaS "dashboard" look to embrace a high-end editorial aesthetic. Our Creative North Star is **The Architectural Authority**. We treat digital space like a physical gallery: expansive, structured by light and shadow rather than lines, and anchored by commanding typography.

To break the "template" feel, we employ **Intentional Asymmetry**. Instead of centering every element, we use the spacing scale to create weighted layouts where content breathes. We utilize overlapping elements—such as a `surface-container-lowest` card bleeding over a `primary-container` hero section—to create a sense of tactile depth and bespoke craftsmanship.

---

## 2. Color Strategy & Atmospheric Depth
Our palette is rooted in deep, authoritative blues, contrasted by vibrant, energetic accents. We don't just "fill" shapes; we create atmosphere.

### The "No-Line" Rule
**Standard 1px solid borders are strictly prohibited for sectioning.** Structural boundaries must be defined exclusively through background color shifts or tonal transitions.
- Use `surface` (#f6faff) for the main page canvas.
- Use `surface-container-low` (#f0f4f9) for secondary sidebar or utility areas.
- Use `surface-container-highest` (#dfe3e8) for embedded code blocks or subtle inset areas.

### Surface Hierarchy & Nesting
Think in layers. A `surface-container-lowest` (#ffffff) card should sit atop a `surface-container-low` (#f0f4f9) section. This "paper-on-table" nesting creates natural hierarchy without visual clutter.

### The "Glass & Gradient" Rule
To elevate the UI from "flat" to "premium," use Glassmorphism for floating navigation bars or overlay modals.
- **Glass Token:** `surface` at 70% opacity with a `20px` backdrop-blur.
- **Signature Textures:** Main CTAs should not be flat. Use a linear gradient from `primary` (#001928) to `primary-container` (#002f46) at a 135-degree angle to provide "soul" and depth.

---

## 3. Typography: The Editorial Voice
We use a high-contrast typographic scale to establish immediate authority.

*   **Display & Headlines (Manrope):** Our "Commanding" voice. Use `display-lg` (3.5rem) with a `tight` letter-spacing (-0.02em) for hero sections. The geometric nature of Manrope feels cutting-edge and professional.
*   **Body & Labels (Inter):** Our "Functional" voice. Inter provides maximum readability at smaller scales. For `body-md`, ensure a line-height of 1.6 to maintain the "clean white space" vibe.
*   **The Power Ratio:** Headlines should always be significantly heavier and larger than body text. Never settle for "middle-ground" sizing; if a headline is important, let it dominate the frame.

---

## 4. Elevation & Tonal Layering
We convey importance through **Tonal Layering** rather than traditional structural dividers.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface-container-lowest` card on a `surface` background creates a soft, natural lift.
*   **Ambient Shadows:** When a "floating" effect is required (e.g., for a high-conversion pop-over), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(0, 25, 40, 0.06)`. Note the use of a `primary` tint in the shadow—never use pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` (#c2c7cd) at **15% opacity**. It should be felt, not seen.
*   **Roundedness Scale:**
    *   **Default (8px):** For standard inputs and small cards.
    *   **LG (16px):** For primary content containers.
    *   **Full:** Reserved exclusively for Pills and Chips.

---

## 5. Components

### Buttons
- **Primary:** Gradient (`primary` to `primary-container`), white text, `Default` roundedness. Subtle scale-down effect (0.98) on click.
- **Secondary:** `surface-container-lowest` with a "Ghost Border." High-contrast `on-surface` text.
- **Tertiary:** No background. Underline appears only on hover. Use for "Learn More" links.

### Input Fields
- **Styling:** `surface-container-lowest` background with a subtle `outline-variant` ghost border. 
- **States:** On focus, the border transitions to `secondary` (#34647a) with a 4px soft glow (outer shadow).
- **Forbid:** Do not use dark backgrounds for inputs; keep them bright and "high-trust."

### Cards & Lists
- **The "No-Divider" Rule:** Forbid horizontal lines between list items. Use `Spacing 4` (1.4rem) to separate items or a `surface-container-low` hover state to define boundaries.
- **Data Tables:** Use alternating background shifts (`surface` and `surface-container-low`) instead of grid lines.

### Signature Component: The "Lead-Card"
A bespoke component for this system: A `surface-container-lowest` card with a `3.5rem` left-padding, featuring a vertical accent bar of `tertiary-container` (#5f0011) to highlight "High-Intent" data points.

---

## 6. Do's and Don'ts

### Do
- **Do** use `Spacing 16` and `20` to create massive breaks between major sections.
- **Do** use `secondary-container` (#b4e4fd) for subtle background highlights behind important icons.
- **Do** align typography to a strict baseline grid to maintain the "Architectural" feel.

### Don't
- **Don't** use 1px solid borders to separate the header from the body; use a background shift or a "Glass" blur.
- **Don't** use pure black (#000000) for text. Always use `on-surface` (#171c20).
- **Don't** crowd components. If it feels "busy," double the padding. High-trust equates to a lack of visual anxiety.