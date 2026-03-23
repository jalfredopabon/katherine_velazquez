# Design System Document

## 1. Overview & Creative North Star: "The Clinical Atelier"
This design system is anchored by the Creative North Star of **"The Clinical Atelier."** It represents the intersection of rigorous medical precision and high-end editorial luxury. We are moving away from the "template-heavy" medical industry standard toward a digital experience that feels bespoke, serene, and authoritative.

The visual identity breaks the traditional rigid grid through **intentional asymmetry** and **breathable compositions**. By utilizing generous whitespace and high-contrast typography scales, we create an environment where information is not just read, but "curated." This system prioritizes the feeling of a premium physical space—clean surfaces, soft lighting, and tactile depth.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule
The palette is rooted in a soft, warm clinical base with metallic accents that signify prestige.

### The "No-Line" Rule
To maintain a high-end aesthetic, **designers are prohibited from using 1px solid borders for sectioning.** Structural boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section should sit directly against a `surface` background to create a sophisticated, borderless transition.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine vellum.
- **Surface (`#f9f9f9`):** The foundation.
- **Surface-Container-Low (`#f3f3f3`):** Use for large secondary content blocks.
- **Surface-Container-Lowest (`#ffffff`):** Use for elevated interactive cards to provide a "pop" against the background.

### The "Glass & Gradient" Rule
To move beyond a flat digital feel, use **Glassmorphism** for floating elements (e.g., sticky headers or mobile navigation). Apply semi-transparent surface colors with a `backdrop-blur` of 20px. 
- **Signature Gradients:** For primary CTAs, utilize a subtle linear gradient from `primary` (`#8a4853`) to `primary-container` (`#a6606b`) at a 135-degree angle. This adds "soul" and a metallic shimmer reminiscent of rose gold.

---

## 3. Typography: Editorial Authority
The typography system uses a high-contrast pairing to balance clinical expertise with lifestyle luxury.

- **Display & Headlines (Noto Serif):** These are our "Editorial" voices. Use `display-lg` (3.5rem) with tight letter-spacing for hero sections to establish an immediate sense of premium quality. 
- **Titles & Body (Inter):** These are our "Functional" voices. Use `body-lg` (1rem) with a generous line-height (1.6) to ensure the clinical information feels approachable and airy.
- **Labels:** Use `label-md` in all-caps with increased letter-spacing (0.05em) when referencing medical grades or technical specifications to maintain a professional "lab-labeled" look.

---

## 4. Elevation & Depth: Tonal Layering
We eschew traditional drop shadows in favor of **Tonal Layering** and **Ambient Light.**

- **The Layering Principle:** Achieve depth by "stacking" surface tiers. A `surface-container-lowest` card placed on a `surface-container-low` section creates a soft, natural lift without the need for heavy shadows.
- **Ambient Shadows:** When a floating effect is required (e.g., a booking modal), use a diffused shadow: `box-shadow: 0 20px 40px rgba(47, 49, 49, 0.04)`. The shadow color is a tint of the `on-surface` color, never pure black.
- **The "Ghost Border" Fallback:** If a container requires a boundary for accessibility, use a "Ghost Border": `outline-variant` (`#d7c1c3`) at **15% opacity**.
- **Frosted Integration:** Use `surface-blur` for overlays to allow background colors to bleed through, ensuring the layout feels integrated rather than "pasted on."

---

## 5. Components: Bespoke Elements

### Buttons
- **Primary (Rose Gold):** Uses `primary` (`#8a4853`) with `on-primary` (`#ffffff`) text. Apply `rounded-md` (0.375rem) and a subtle 300ms transition on hover.
- **Secondary (Champagne/Charcoal):** Use `secondary` (`#5f5e5e`) or `tertiary` (`#735c00`) for low-priority actions.
- **Tertiary:** Text-only with a `label-md` style and a subtle underline that expands on hover.

### Input Fields
- **Styling:** No background. Use a bottom-only "Ghost Border" (15% opacity `outline-variant`). On focus, the border transitions to 100% opacity `primary`.
- **Labels:** Always use `label-sm` floating above the input to maintain a clean, architectural look.

### Cards & Lists
- **Rule:** Forbid the use of horizontal divider lines.
- **Execution:** Separate list items using the Spacing Scale (`8` or `10`). For cards, use background color shifts (`surface-container-lowest`) rather than borders to define the container.

### Clinical Progress Indicators (Context Specific)
- **The "Aesthetic Timeline":** A custom component using thin lines and `tertiary` (`#735c00`) dots to track patient journeys. It should feel like a high-end jewelry brand's timeline.

---

## 6. Do's and Don'ts

### Do
- **Do** use asymmetrical image placements to create an editorial, magazine-like feel.
- **Do** utilize `spacing-20` and `spacing-24` for section padding to allow the design to "breathe."
- **Do** use `notoSerif` for any text that is meant to be emotive or aspirational.

### Don't
- **Don't** use 100% black (`#000000`). Always use `secondary` (`#2E2E2E`) for high-contrast text.
- **Don't** use "Standard" shadows. If you can clearly see where the shadow ends, it is too heavy.
- **Don't** use sharp 90-degree corners. Even a `sm` (0.125rem) radius is required to soften the "clinical" edge into a "welcoming" one.
- **Don't** crowd the interface. If a screen feels "busy," increase the whitespace scale by two levels.