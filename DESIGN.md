# Design System Documentation: Industrial Precision & Editorial Depth

## 1. Overview & Creative North Star
### Creative North Star: "The Tectonic Shift"
In the world of heavy engineering, weight is synonymous with value. This design system departs from the flimsy, "airy" aesthetics of typical SaaS products to embrace **Tectonic Layering**. We treat the UI not as a flat screen, but as a series of heavy, interlocking plates. 

By utilizing intentional asymmetry, oversized "Display" typography, and a "No-Line" philosophy, we create an editorial-grade experience that mirrors the power of XCMG machinery. We trade generic borders for sophisticated tonal shifts, ensuring the interface feels as engineered and high-trust as a 400-ton excavator.

---

## 2. Colors & Surface Philosophy
The palette is rooted in industrial utility, using high-visibility safety yellow and deep hydraulic blue.

### The "No-Line" Rule
**Explicit Instruction:** Sectioning via 1px solid borders is strictly prohibited. 
Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` (#f3f4f5) sidebar must sit against a `surface` (#f8f9fa) main stage. This forces a cleaner, more sophisticated architectural feel.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of metal and glass. 
- **Base Layer:** `surface` (#f8f9fa)
- **Secondary Plates:** `surface-container-low` (#f3f4f5) for subtle groupings.
- **Interactive Elevated Cards:** `surface-container-lowest` (#ffffff) to provide "pop" against gray backgrounds.
- **Tertiary Information:** `surface-container-high` (#e7e8e9) for nested utility panels.

### The "Glass & Gradient" Rule
To avoid a "flat" corporate look, use Glassmorphism for floating overlays (e.g., calculator widgets or sticky mobile headers). Use semi-transparent surface colors with a `backdrop-blur` of 12px–20px. 
**Signature Texture:** Apply a subtle linear gradient to Primary CTAs, transitioning from `primary` (#7c5800) to `primary-container` (#fdb913). This adds a metallic "sheen" reminiscent of industrial paint.

---

## 3. Typography
We use **Inter** for its technical precision and superior Cyrillic legibility. The scale is exaggerated to create a clear editorial hierarchy.

*   **Display (lg/md/sm):** Used for machine model numbers and hero headlines. It should feel massive and authoritative.
*   **Headline (lg/md):** Used for technical categories (e.g., "Earthmoving Equipment").
*   **Title (lg/md):** Used for card titles and section headers.
*   **Body (lg/md):** Optimized for technical specifications and long-form descriptions. Use `body-md` (0.875rem) for spec tables to maintain density.
*   **Label (md/sm):** Reserved for metadata and button text. Always set in semi-bold for "heavy-duty" readability.

---

## 4. Elevation & Depth
Depth in this system is achieved through **Tonal Layering** rather than structural shadows.

### The Layering Principle
Stacking `surface-container` tiers creates a soft, natural lift. Place a `surface-container-lowest` card on a `surface-container-low` section. This mimics the way architectural blueprints use shading to denote height.

### Ambient Shadows
Where floating elements (like modals) are necessary, use **Ambient Shadows**:
- **Color:** `on-surface` (#191c1d) at 6% opacity.
- **Blur:** 24px to 40px.
- **Offset:** 8px Y-axis.
- This creates a soft "glow" of depth rather than a harsh, dated drop shadow.

### The "Ghost Border" Fallback
If accessibility requires a container boundary, use a **Ghost Border**: the `outline-variant` (#d5c4ac) token at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Multi-Level Sidebar
*   **Background:** `surface-container-low` (#f3f4f5).
*   **Active State:** Use a 4px vertical "tab" of `primary-container` (#fdb913) on the leading edge. No background color change on the item itself; just a shift in text weight to `label-md` Bold.

### Spec Cards (Heavy Duty)
*   **Container:** `surface-container-lowest` (#ffffff) with a `DEFAULT` (0.25rem) corner radius.
*   **Content:** Forbid dividers. Use 24px of vertical whitespace between spec categories.
*   **Data Points:** Label in `label-sm` (Anthracite 60% opacity), Value in `body-md` Bold (Anthracite 100%).

### Calculator Widgets
*   **Style:** Glassmorphic. Background: `surface/80%` with a 16px backdrop blur.
*   **Inputs:** `surface-variant` (#e1e3e4) background with a 2px bottom-only focus stroke in `secondary` (#185eb0).

### Buttons
*   **Primary:** `primary` (#7c5800) background, `on-primary` (#ffffff) text. Use `xl` (0.75rem) roundedness for a modern touch against industrial edges.
*   **Secondary:** Ghost style. No background, `outline` (#837560) at 20% opacity for the stroke.
*   **Tertiary:** Plain text with `secondary` (#185eb0) color and an arrow icon (→).

### Inputs & Form Fields
*   **Resting:** `surface-container-highest` (#e1e3e4) with no border.
*   **Focus:** A subtle "glow" using `secondary-container` (#70a6fe) at 30% opacity.

---

## 6. Do's and Don'ts

### Do
*   **DO** use whitespace as a separator. If elements feel cluttered, increase the gap before considering a line.
*   **DO** use "Tectonic Overlaps"—let machine images slightly overlap the boundary of the section below them to create 3D depth.
*   **DO** prioritize high-contrast typography for technical specs to ensure readability in field conditions.

### Don't
*   **DON'T** use 100% black. Always use `on-surface` (#191c1d) or `inverse_surface` (#2e3132) for a more premium, "Anthracite" feel.
*   **DON'T** use "Standard Blue" for links. Use the brand `secondary` (#185eb0) or `on-secondary-container` (#003b77).
*   **DON'T** use rounded corners larger than `xl` (0.75rem). This is an industrial system; it should feel sturdy and geometric, not bubbly or "soft."