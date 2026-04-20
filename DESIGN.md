# Design System Strategy: The Institutional Luminary

## 1. Overview & Creative North Star
**Creative North Star: The Sovereign Architect**

This design system moves away from the "retail crypto" aesthetic of chaotic neon and cluttered charts. Instead, it adopts the persona of a **Sovereign Architect**: a silent, powerful force that conveys institutional authority through restraint and structural precision. 

The system breaks the "template" look by utilizing intentional asymmetry—placing high-density data visualization against vast expanses of "Negative Deep Space" (`surface-dim`). We prioritize an editorial layout where typography scale does the heavy lifting, and depth is communicated through light and translucency rather than physical dividers. We are not just building a dashboard; we are building a digital vault.

---

## 2. Colors & Atmospheric Depth
Our palette is rooted in the deep void of institutional finance, punctuated by "electric" data points.

*   **The "No-Line" Rule:** We do not use 1px solid borders to section content. To separate a sidebar from a main feed, transition from `surface` (#071326) to `surface-container-low` (#0F1C2F). Boundaries are felt through tonal shifts, not seen through lines.
*   **Surface Hierarchy & Nesting:** Treat the UI as layers of polished obsidian. 
    *   **Base:** `surface` (The foundation).
    *   **Sections:** `surface-container-low` (Subtle grouping).
    *   **Interactive Cards:** `surface-container-high` (Emerging from the depths).
*   **The "Glass & Gradient" Rule:** Floating elements (modals, dropdowns) must use Glassmorphism. Apply `surface-container-highest` at 60% opacity with a `backdrop-blur` of 20px. 
*   **Signature Textures:** For primary CTAs and hero highlights, use a linear gradient: `primary-container` (#1D64F2) to a 20% glow of `primary` (#B3C5FF) at a 135-degree angle. This adds a "backlit" soul to the interface.

---

## 3. Typography: The Authority of Scale
We utilize a high-contrast typographic pairing to balance technical precision with institutional heritage.

*   **Display & Headlines (Space Grotesk / Ataero):** These are our "Structural" fonts. Used for large headers (`display-lg` to `headline-sm`), they should feel architectural. Use `on-surface` for maximum readability. In hero sections, experiment with `0.02em` letter spacing to increase the "premium" feel.
*   **Body & Labels (Inter):** The "Utility" font. Inter provides extreme legibility for complex financial data. 
    *   Use `body-md` for standard text.
    *   Use `label-md` in all-caps with `0.05em` tracking for category headers to signify "Institutional Tagging."
*   **Visual Hierarchy:** Establish authority by pairing a massive `display-lg` metric with a tiny, high-contrast `label-sm` descriptor. The gap in scale creates a sophisticated, editorial rhythm.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden. We use "Ambient Glows" and "Tonal Lifts."

*   **The Layering Principle:** To lift a card, move it up the token scale. An asset card should be `surface-container-highest` (#29354A) sitting on a `surface-container-low` (#0F1C2F) background.
*   **Ambient Shadows:** If a component must float (e.g., a hover state), use a shadow color derived from `surface-tint` (#B3C5FF) at 5% opacity, with a 40px blur and 20px Y-offset. It should look like light escaping from behind a heavy object.
*   **The "Ghost Border" Fallback:** If a layout feels too "bleary," use a 1px border with `outline-variant` (#424655) at **15% opacity**. It should be barely perceptible—a "ghost" of a boundary.

---

## 5. Components

### Buttons
*   **Primary:** Gradient fill (`primary-container` to `primary`). No border. `xl` (0.75rem) corner radius. 
*   **Secondary:** Ghost style. `outline-variant` at 20% opacity border. Text in `primary`.
*   **State:** On hover, apply a subtle outer glow using the `surface-tint` shadow mentioned in Section 4.

### Cards & Lists
*   **Card Anatomy:** Never use a divider line. Use a `1.5rem` vertical spacing gap or a slight shift to `surface-container-highest` for the header of the card.
*   **Lists:** Forfeit the 1px row separator. Use alternating background tints (`surface` vs `surface-container-lowest`) or simply generous `body-lg` line-height to create clear scanability.

### Input Fields
*   **Style:** `surface-container-low` fill. No bottom line. 
*   **Focus State:** The border transitions to `primary` (#B3C5FF) at 30% opacity with a subtle 4px "bloom" (glow) effect.

### Chips & Tags
*   **Style:** Use `secondary-container` (#3A475E) with `on-secondary-container` (#A8B6D1) text. Keep corners `full` for a pill shape to contrast against the structural `xl` corners of the cards.

### High-End Additions (The "Director's Cut")
*   **The Data Glow:** When displaying "Profit" metrics, don't just use green text. Use a tiny radial gradient glow behind the text to make the numbers feel "alive."
*   **The Glass Header:** The main navigation should be a `surface-container-lowest` bar at 70% opacity with a heavy backdrop blur, pinned to the top, creating a "frosted lens" over the content as the user scrolls.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins (e.g., a wider left margin than right) to create a custom, high-end editorial feel.
*   **Do** lean into "Deep Space." Let the `surface-dim` background breathe. 
*   **Do** use `primary` accents sparingly. If everything glows, nothing is important.

### Don’t:
*   **Don’t** use pure black (#000000). Use our `surface` (#071326) to maintain "Atmospheric Depth."
*   **Don’t** use standard "Success Green" or "Warning Red" if they clash with the cyan/blue vibe. Use the `error` (#FFB4AB) and `primary` scales provided.
*   **Don’t** use dividers or "boxes inside boxes." Use space and tonal shifts to define ownership of content.