# Design System: High-Performance Athletic Intelligence

## 1. Overview & Creative North Star: "The Kinetic Lab"
This design system is built to bridge the gap between elite sports science and high-end editorial storytelling. Our Creative North Star is **"The Kinetic Lab"**—a visual environment that feels like a high-stakes film session under stadium lights. 

We move beyond the "SaaS dashboard" look by embracing **Precision Brutalism**. This means rejecting standard borders and generic grids in favor of intentional asymmetry, high-contrast typography scales, and tonal layering. The interface doesn't just display data; it captures the momentum of an athlete in flight. Every element should feel engineered, yet premium and aspirational.

---

## 2. Color & Atmospheric Depth
Our palette is rooted in the darkness of the "film room," punctuated by the "electric" energy of performance peaks.

### The Palette
*   **Core Atmosphere:** `surface` (#0e0e0e) and `surface_container_lowest` (#000000) form our void.
*   **The Electric Pulse:** `primary_container` (#cafd00 - Electric Lime) is our primary driver for action and high-performance metrics.
*   **The PR Celebration:** `secondary` (#fdbf35 - High-Voltage Gold) is reserved for "Personal Record" moments, elite achievements, and gold-standard benchmarks.
*   **Functional Alerts:** `error` (#ff7351) handles fatigue warnings or technical failures with a warm, urgent glow.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. We define space through "Tonal Carving." A card is not a box with an outline; it is a `surface_container` (#1a1a1a) sitting on a `surface` (#0e0e0e) background. The transition in hex value is the border.

### The "Glass & Gradient" Rule
To evoke the "Sports Science" lens, use Glassmorphism for floating overlays (e.g., player stat tooltips). Use `surface_variant` at 60% opacity with a `20px` backdrop blur. 
*   **Signature Polish:** Apply a subtle linear gradient to main CTAs from `primary` (#f3ffca) to `primary_dim` (#beee00) at a 135° angle. This adds a "machined" metallic sheen that flat colors lack.

---

## 3. Typography: Editorial Authority
We use typography to create a rhythm between "The Athlete" (Display) and "The Analytics" (Body).

*   **Display & Headlines (Space Grotesk):** This is our "modern varsity." The wide, geometric architecture of Space Grotesk should be used at `display-lg` (3.5rem) to command attention. Use tight letter-spacing (-0.02em) for headlines to mimic high-impact sports journalism.
*   **Body & Data (Inter):** For complex analytics, Inter provides the "Science Lab" precision. It is ultra-clean and disappears, allowing the data to speak.
*   **Labels (Lexend):** Used for technical metadata and small UI labels. Lexend’s increased legibility ensures that even at `label-sm` (0.6875rem), performance stats are unmistakable.

---

## 4. Elevation & Depth: Tonal Layering
In a dark-mode dominant system, traditional drop shadows are often invisible or "muddy." We use **Tonal Layering** to create hierarchy.

### The Layering Principle
Stack containers to define importance:
1.  **Level 0 (Base):** `surface` (#0e0e0e) - The stadium floor.
2.  **Level 1 (Sections):** `surface_container_low` (#131313) - Large content areas.
3.  **Level 2 (Cards):** `surface_container` (#1a1a1a) - Individual data points.
4.  **Level 3 (Pop-overs):** `surface_bright` (#2c2c2c) - Active states or modals.

### Ambient Shadows & Ghost Borders
*   **Shadows:** If a card must "float," use a large 32px blur at 8% opacity using the `on_background` (#ffffff) color. This creates a "glow" rather than a shadow, mimicking light reflecting off a dark surface.
*   **The Ghost Border:** For accessibility in complex data tables, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons: The "Ignition" Variants
*   **Primary:** Background: `primary_container` (#cafd00). Text: `on_primary_fixed` (#3a4a00). Shape: `md` (0.375rem). The contrast here is violent and intentional; it is the "Start Session" button.
*   **Secondary:** Background: `none`. Border: "Ghost Border" (15% `outline_variant`). Text: `on_surface`.
*   **Tertiary:** Text only, in `primary_dim` (#beee00), capitalized, with a `0.1rem` letter spacing.

### Cards & Lists: The Kinetic Feed
*   **Structure:** No dividers. Use `Spacing 8` (1.75rem) to separate list items. 
*   **Interaction:** On hover, a card should shift from `surface_container` to `surface_container_high`.
*   **Data Points:** Large numeric values should always use `display-sm` in `primary` to emphasize performance.

### Input Fields: The "Sensor" Style
*   **Default:** `surface_container_highest` background with a bottom-only "Ghost Border."
*   **Focus State:** The bottom border transforms into a 2px `primary_container` line, accompanied by a subtle `primary` outer glow (4px blur).

### Specialized Component: The "Trajectory Legend"
*   **Function:** A small, floating widget showing kinetic motion lines or arcs. 
*   **Style:** Use `tertiary_container` (#fce047) for trajectory paths to differentiate from the Lime Green of the primary UI.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Align text to the left but place data-visualizations slightly off-center to create a sense of motion.
*   **Use Kinetic Motifs:** Use `outline_variant` to draw subtle 45-degree "grid lines" in the background of hero sections.
*   **High Contrast:** Ensure all "Electric Lime" elements are paired with the darkest `surface` tokens for maximum "pop."

### Don’t:
*   **Don't use Rounded Corners `full`:** Except for small status pips. This system is about "Edge." Stick to `md` (0.375rem) or `none`.
*   **Don't use Purple or Blue Gradients:** This is not a generic tech app. If you need a secondary color, use the `secondary` Gold or `tertiary` Sand tokens.
*   **Don't Over-shadow:** If the layout feels flat, change the background color of the container instead of adding a shadow.