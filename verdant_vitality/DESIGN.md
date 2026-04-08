# Design System Strategy: High-End Editorial Performance

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Athletic Editor."** 

We are moving away from the generic "app-on-a-grid" look. Instead, this system treats the UI as a premium fitness journal—mixing the authoritative, bold weight of the athletic logo with the airy, sophisticated whitespace of a luxury editorial brand. The goal is to convey "Precision Health" through intentional asymmetry, overlapping elements that suggest movement, and a hierarchy that prioritizes breathing room over information density.

We break the "template" look by using exaggerated typography scales and "tonal layering," ensuring the digital experience feels as custom and premium as a personalized nutrition plan.

---

## 2. Colors & Atmospheric Depth
Our palette is rooted in the Deep Forest Green of the brand, supported by "high-energy" lime accents and a sophisticated neutral foundation.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders for sectioning. Structural boundaries must be defined solely through:
1.  **Background Color Shifts:** Placing a `surface-container-low` (#f3f4f3) section directly against a `surface` (#f9f9f8) background.
2.  **Negative Space:** Using the spacing scale to create distinct visual groups.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. We use the Material surface tokens to create a "nested" depth:
*   **Base Layer:** `surface` (#f9f9f8) for the main canvas.
*   **In-Page Sections:** `surface-container-low` (#f3f4f3) for secondary content zones.
*   **Active Cards:** `surface-container-lowest` (#ffffff) to provide the highest contrast against the off-white base.

### The "Glass & Gradient" Rule
To elevate the startup aesthetic, use **Glassmorphism** for floating headers or navigation bars. Use semi-transparent `surface` colors with a `backdrop-blur` of 20px. 
*   **Signature Textures:** For main CTAs and Hero backgrounds, apply a subtle linear gradient: `primary` (#03271a) to `primary-container` (#1b3d2f). This creates a "velvet" depth that flat hex codes cannot replicate.

---

## 3. Typography: Authority & Legibility
The typography pairing reflects the brand's dual nature: Bold athleticism and scientific precision.

*   **Display & Headlines (Lexend):** A modern, geometric sans-serif that echoes the logo’s bold confidence. We use `display-lg` (3.5rem) to create editorial "moments" where the text becomes a visual graphic element.
*   **Body & Labels (Manrope):** Chosen for its exceptional legibility across English, Russian, and Uzbek. Its slightly condensed nature feels professional and high-tech.
*   **The Weight Contrast:** Always pair a `headline-lg` (Lexend, Bold) with a `body-md` (Manrope, Medium). This high-contrast pairing is the secret to the "Apple-level" premium feel.

---

## 4. Elevation & Depth
We eschew traditional drop shadows for **Tonal Layering**.

### The Layering Principle
Depth is achieved by "stacking" surface tiers. A `surface-container-lowest` card placed on a `surface-container` background creates a natural lift. This mimics fine stationery rather than plastic digital components.

### Ambient Shadows
When a floating element (like a FAB or a Modal) is required, use **Ambient Shadows**:
*   **Color:** Use a tinted version of `on-surface` (#191c1c) at 6% opacity.
*   **Blur:** High diffusion (minimum 40px blur) with a 10px Y-offset. It should feel like a soft glow, not a hard shadow.

### The "Ghost Border" Fallback
If a container requires a boundary (e.g., in a high-density meal plan table), use a **Ghost Border**: The `outline-variant` (#c1c8c2) token at **15% opacity**. Never use 100% opaque lines.

---

## 5. Components
All components feature a large `DEFAULT` radius (1rem) or `lg` (2rem) to soften the "industrial" feel of fitness apps.

*   **Primary Buttons**: Use the `primary` (#03271a) background with `on-primary` (#ffffff) text. Styling should be `rounded-full` with high horizontal padding (e.g., 32px) to create a "pill" shape.
*   **Nutrition Chips**: Used for macros (Proteins, Carbs, Fats). Use `secondary-container` (#bbf244) for a "high-energy" highlight. No borders; just tonal backgrounds.
*   **Input Fields**: `surface-container-high` (#e7e8e7) backgrounds with no borders. On focus, transition to a `ghost border` using the `primary` color at 20% opacity.
*   **Cards**: Forbid the use of divider lines. Separate "Meal Name" from "Calories" using vertical white space or a font-weight shift.
*   **Progress Indicators**: For fitness tracking, use a `secondary` (#4a6700) lime-mint stroke against a `surface-variant` (#e1e3e2) track.
*   **Language Switcher**: A subtle `surface-container-low` pill with `label-md` typography to handle EN, RU, and UZ seamlessly.

---

## 6. Do's and Don'ts

### Do
*   **DO** use whitespace as a functional tool. If a screen feels "busy," increase the padding rather than adding a divider.
*   **DO** use the `secondary` (lime) color sparingly—only for "healthy" cues, success states, or primary conversion points.
*   **DO** ensure all Lexend headlines are set with tight letter-spacing (-2%) to mimic the logo's compact, powerful feel.

### Don't
*   **DON'T** use pure black (#000000). Use `on-background` (#191c1c) for all text to maintain the premium, soft-touch aesthetic.
*   **DON'T** use sharp corners. Every component must use at least the `sm` (0.5rem) radius to maintain the brand's approachable, healthy personality.
*   **DON'T** use standard "blue" for links. Use the `primary` green with an underline or the `secondary` lime for interaction cues.