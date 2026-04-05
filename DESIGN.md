# Design System Documentation: The High-Performance Portfolio

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Precision Curator."** 

In a world of cluttered portfolios, this system stands apart through extreme intentionality and editorial rigor. It rejects the "template" look by treating the screen as a high-end gallery space rather than a generic digital container. We achieve "High-Performance" not through aggressive animations, but through instant cognitive clarity, asymmetric layouts that guide the eye, and a sophisticated interplay between "Manrope" (architectural) and "Inter" (functional) typography. The result is a system that feels engineered yet bespoke—perfect for a developer who values design, or a designer who respects engineering.

---

## 2. Colors & Tonal Architecture
The palette is built on a sophisticated foundation (`neutral_color_hex`) punctuated by a singular, authoritative accent (`primary_color_hex`) and supporting hues (`secondary_color_hex`, `tertiary_color_hex`).

### The "No-Line" Rule
Standard UI relies on 1px borders to separate content. In this system, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through background color shifts. 
- Use appropriately lighter/darker shades of `neutral_color_hex` for sections sitting atop a base background to define content blocks.
- Use `primary_color_hex` or `secondary_color_hex` for high-priority callouts.

### Surface Hierarchy & Nesting
Think of the UI as a series of physical layers—like stacked sheets of heavy-stock vellum. 
- **Base Layer:** The `neutral_color_hex` (light gray: #D9E2EC) serves as the primary surface.
- **Secondary Containers:** Use a slightly darker shade of `neutral_color_hex` for content blocks.
- **Nested Content/Cards:** Use a lighter shade of `neutral_color_hex` or pure white for a soft, natural lift.

### Signature Textures & Glassmorphism
To avoid a "flat" or "cheap" feel, use **Glassmorphism** for navigation bars or floating action menus. 
- **Token:** A slightly darker shade of `neutral_color_hex` at 80% opacity with a `20px` backdrop-blur.
- **CTA Gradient:** For primary buttons or hero accents, use a subtle linear gradient from `primary_color_hex` (#102A43) to a slightly darker shade of `primary_color_hex` to provide a "jeweled" depth that flat hex codes lack.

---

## 3. Typography
We utilize a dual-typeface system to balance editorial personality with technical readability.

- **The Architect (Manrope):** Used for headlines and titles. Manrope’s geometric nature provides a modern, high-end feel.
- **The Engineer (Inter):** Used for body text and labels. Inter is the industry standard for readability; it communicates precision and technical competence.

**Editorial Scaling:** Don't be afraid of large scale headlines. Use them for hero statements to create an immediate impact, contrasting them sharply with smaller body text for a high-contrast, premium look.

---

## 4. Elevation & Depth
In this system, depth is a function of light and tone, not structural lines.

### The Layering Principle
Achieve hierarchy by stacking surface tiers. A `primary_color_hex` or `secondary_color_hex` element on a `neutral_color_hex` background creates an immediate focal point without requiring a single drop shadow.

### Ambient Shadows
Shadows should be invisible but felt. If a "floating" effect is required (e.g., a modal or floating card):
- **Blur:** 32px – 64px.
- **Opacity:** 4% – 6%.
- **Color:** Use a dark shade from the `primary_color_hex` palette rather than pure black to keep the shadow feeling "ambient" and natural.

### The "Ghost Border" Fallback
When accessibility or high-density layouts require a container boundary, use a **Ghost Border**:
- **Token:** A very light tint of `primary_color_hex` at 15% opacity.
- **Width:** 1px.
- **Constraint:** Never use 100% opaque borders.

---

## 5. Components

### Buttons
- **Primary:** `primary_color_hex` background with a contrasting light text color. Apply the `0` roundedness (sharp, angular) for a "high-performance" look. 
- **Secondary:** A lighter shade of `neutral_color_hex` background. No border.
- **Hover States:** Instead of a simple color change, use a `0.2s ease` transition to shift the background to a slightly darker shade of its original color.
- **Corner Logic:** Use `0` roundedness (sharp, angular) for all elements to maintain a consistent "high-performance/sharp" aesthetic.

### Input Fields
- **Base:** Use a lighter shade of `neutral_color_hex` with a 1px border in a very light tint of `primary_color_hex` at 20% opacity.
- **Active State:** Shift the border to `primary_color_hex` (100% opacity) and add a subtle 2px glow using the `primary_color_hex` color at 10% opacity.
- **Typography:** Labels must use `label_font` in a slightly darker shade of `primary_color_hex`.

### Chips (Tags)
- **Style:** A darker shade of `neutral_color_hex` background with a contrasting text color.
- **Rounding:** Always use maximum roundedness for chips (pill-shaped) to contrast with the sharp, angular structural elements of the layout.

### Cards & Projects
- **Constraint:** **Strictly forbid divider lines.** 
- **Separation:** Use vertical white space (3rem+) and distinct shades of `neutral_color_hex` to separate project details. 
- **Hover:** On project cards, use a subtle lift—scale to 101% and increase the Ambient Shadow opacity from 4% to 8%.

---

## 6. Do's and Don'ts

### Do:
- **Embrace Asymmetry:** Place a large headline on the left and a small body description on the right with significant horizontal gap.
- **Use "White" Space as a Tool:** Treat empty space as an active element of the design to reduce cognitive load.
- **Reference Tonal Tokens:** Always use `primary_color_hex`, `secondary_color_hex`, `tertiary_color_hex`, and `neutral_color_hex` and their respective tints/shades for depth instead of hard-coding hex values.

### Don't:
- **No 1px Dividers:** Never use a horizontal line to separate sections. Use a background color change or 80px+ of white space.
- **No "Default" Shadows:** Avoid the standard CSS `box-shadow: 0 2px 4px rgba(0,0,0,0.5)`. It feels dated and heavy.
- **No Pure Black Text:** Use a dark shade derived from `primary_color_hex` for body text. It is softer on the eyes and feels more sophisticated than #000000.
- **No Complex Motion:** Avoid "bouncing" or "sliding" animations. Use simple opacity fades (200ms) to maintain a professional, efficient atmosphere.