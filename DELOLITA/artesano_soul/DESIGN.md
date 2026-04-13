# Design System Strategy: The Artisanal Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Soulful Alchemist."** 

We are not building a standard coffee app; we are crafting a digital invitation into a high-end Colombian bakery. This system moves away from the "industrial-grid" look of modern tech, opting instead for an **Editorial Narrative** style. By utilizing intentional asymmetry, cinematic negative space, and overlapping elements, we create a sense of movement and warmth. The UI should feel like a premium lifestyle magazine—organic, sophisticated, and deeply rooted in the "B Corp" spirit of social responsibility.

## 2. Colors & Tonal Depth
The palette is rooted in the earth and the bean: warm caramels (`primary`), soft blushes (`secondary`), and the deep richness of espresso (`on-primary-fixed`).

### The "No-Line" Rule
**Strict Mandate:** Traditional 1px solid borders are prohibited for sectioning. 
Boundaries must be defined solely through background color shifts. To separate a testimonial section from a product gallery, transition from `surface` to `surface-container-low`. This creates a seamless, high-end "stitched" feel rather than a fragmented layout.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine Colombian paper. 
- **Base:** `surface` (#fff8ef)
- **Secondary Content:** `surface-container-low` (#fbf3e4)
- **Interactive Cards:** `surface-container-lowest` (#ffffff) to provide a soft "pop" against the cream background.
- **Nesting:** When placing a card within a container, use a one-step shift (e.g., a `surface-container-highest` button inside a `surface-container-low` card) to create depth without visual noise.

### The "Glass & Gradient" Rule
To add "soul," use a subtle radial gradient on Hero backgrounds transitioning from `primary` (#714428) to `primary-container` (#8d5b3e). For floating navigation or modal overlays, apply **Glassmorphism**: use `surface` at 80% opacity with a `24px` backdrop-blur. This allows the cinematic imagery to bleed through the UI, softening the brand's digital edges.

## 3. Typography
The typography is an intentional dialogue between Colombian tradition and modern elegance.

*   **Display & Headlines (Noto Serif):** Our "Serif Voice" represents the artisanal, high-end bakery roots. Use `display-lg` with tight letter-spacing for a bold, editorial feel in Hero sections.
*   **Body & Labels (Plus Jakarta Sans):** Our "Sans-Serif Voice" represents the clean, B-Corp professional side of the brand. It provides high legibility for product descriptions and community stories.
*   **The Contrast Play:** Always pair a `headline-md` with a `label-md` in uppercase with 10% letter-spacing. This high-contrast pairing (Serif vs. Sans) is the hallmark of premium editorial design.

## 4. Elevation & Depth
We eschew "techy" shadows in favor of **Tonal Layering** and **Ambient Light**.

*   **The Layering Principle:** Avoid elevation levels 1-5. Instead, achieve depth by stacking `surface-container` tiers. A `surface-container-lowest` card on a `surface-dim` background provides all the "lift" required.
*   **Ambient Shadows:** If a floating action button or a modal requires a shadow, use a diffuse, tinted shadow: `box-shadow: 0 20px 40px rgba(113, 68, 40, 0.08)`. Never use pure black; always tint the shadow with the `primary` espresso/caramel tones.
*   **The Ghost Border:** If a form field or button requires a container for accessibility, use the `outline-variant` token at **15% opacity**. It should be a "whisper" of a line, barely felt, never seen.

## 5. Components

### Buttons
*   **Primary:** Rounded `full` (9999px). Background: `primary`. Text: `on-primary`. Use for main "Order Now" or "Join Community" actions.
*   **Secondary:** Rounded `full`. Background: `secondary-container`. Text: `on-secondary-container`. This soft pink provides a feminine, approachable touch.
*   **Tertiary:** No background. Serif `title-sm` typography with a subtle `primary` underline (2px) offset by 4px.

### Cards & Lists
*   **The Rule of Zero Lines:** Lists must never use divider lines. Use `spacing-lg` (vertical white space) or alternate background tints between `surface` and `surface-container-low` to distinguish items.
*   **Image Cards:** Use `xl` (3rem) rounded corners. Images should have a subtle `primary-fixed` overlay at 5% to keep the warm, cinematic "De Lolita" tone.

### Inputs & Forms
*   **Fields:** Use `surface-container-high` backgrounds with a `none` border. On focus, transition the background to `surface-container-highest` and add the "Ghost Border" (15% `outline-variant`).
*   **Labels:** Always use `label-md` in `on-surface-variant` positioned 8px above the input.

### Signature Components
*   **The "Community Toast":** A soft, floating notification using Glassmorphism (`surface` @ 85% + blur) with a `secondary` accent icon to celebrate socially responsible milestones or brand news.
*   **Cinematic Hero:** A full-bleed image container using the `xl` (3rem) corner radius at the bottom edge only, creating an organic "flow" into the next section.

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts (e.g., a large image on the left, with text slightly overlapping its right edge).
*   **Do** prioritize "Breathing Room." If you think there is enough white space, add 20% more.
*   **Do** use `on-surface-variant` for long-form body text to reduce contrast and increase the "warm/soft" feel.

### Don't
*   **Don't** use 100% black (#000000). Use `on-primary-fixed` (#331200) for your darkest tones.
*   **Don't** use "Standard" 4px or 8px corners. Only use `md` (1.5rem), `lg` (2rem), or `xl` (3rem) to maintain the artisanal, organic personality.
*   **Don't** use hard-edged icons. Use rounded, light-weight strokes that match the `plusJakartaSans` weight.

---
**Director's Note:** Every pixel must feel "hand-poured." If a layout feels too rigid or "square," break the grid. Overlap a coffee bean illustration across two sections. Let a serif heading breathe across 80% of the screen. We are selling the warmth of Colombia, not a software package.