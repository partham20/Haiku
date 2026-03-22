```markdown
# Design System Document

## 1. Overview & Creative North Star: "The Velvet Anthology"
This design system is engineered to transform a mobile poetry-sharing platform into a high-end, immersive digital sanctuary. Moving beyond the "utility-first" look of standard social apps, our Creative North Star is **The Velvet Anthology**. 

We treat every screen as a premium editorial layout where the poem is the hero. By utilizing deep charcoal foundations and high-energy green accents, we create a "low-light gallery" effect. To break the "template" feel, we employ **intentional asymmetry**: text is often offset, images bleed into the edges of the screen, and surface layers overlap with varying levels of transparency to create a sense of physical depth.

---

## 2. Colors: Tonal Depth & The High-Contrast Pulse
The palette is rooted in absolute blacks and layered charcoals to ensure the "Vibrant Green" accents pulse with maximum energy.

### Color Logic
- **Foundational Neutrals:** `surface` (#0e0e0e) and `surface_container_lowest` (#000000) are used for the primary canvas to provide an infinite, immersive void.
- **The Accents:** `primary` (#57f47f) is your "Call to Action" heartbeat. Use it sparingly for high-impact moments like "Publish" or "Follow."
- **Tonal Hierarchy:** Use `on_surface_variant` (#adaaaa) for secondary poetic metadata (dates, stanzas) to ensure the main poem text (`on_surface` #ffffff) commands the user's focus.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to section content. Boundaries must be defined through background color shifts. To separate a poem from a feed, place a `surface_container_low` card on a `surface` background. 

### The Glass & Gradient Rule
For floating playback controls or "Quick Write" buttons, use **Glassmorphism**. Apply `surface_variant` with a 60% opacity and a 20px backdrop-blur. For primary CTAs, apply a subtle linear gradient from `primary` (#57f47f) to `primary_container` (#0ec557) at a 135-degree angle to add "soul" and dimension.

---

## 3. Typography: Editorial Authority
We use a dual-font strategy to balance modern tech with literary sophistication.

- **Display & Headlines (`plusJakartaSans`):** These are your "Statement" styles. Use `display-lg` for poem titles. The wide apertures of Plus Jakarta Sans provide a premium, airy feel that prevents dark mode from feeling claustrophobic.
- **Body & Labels (`manrope`):** For the poems themselves and UI metadata. `body-lg` (1rem) is the standard for poem stanzas. Manrope’s geometric yet warm structure ensures legibility during long-form reading.
- **Hierarchy Tip:** Use `headline-sm` for poet names and `label-sm` for syllable counts or tags. Always maintain high tracking (letter-spacing) on `label` styles to enhance the "luxury" aesthetic.

---

## 4. Elevation & Depth: Tonal Layering
In this design system, height is expressed through light, not shadows.

- **The Layering Principle:** Depth is achieved by "stacking" surface tiers. 
    - *Level 0 (Canvas):* `surface` (#0e0e0e)
    - *Level 1 (Sections):* `surface_container_low` (#131313)
    - *Level 2 (Cards):* `surface_container_high` (#20201f)
- **Ambient Shadows:** Only use shadows for floating modals. Use a blur of 32px, 0px offset, and 8% opacity using the `on_surface` color. This creates a soft "glow" rather than a dirty smudge.
- **The "Ghost Border" Fallback:** If a container sits on an identical color (e.g., a search bar), use the `outline_variant` (#484847) at **15% opacity**. This creates a "whisper" of a boundary that preserves the immersive flow.

---

## 5. Components: Content-First Primitives

### Buttons
- **Primary:** Capsule-shaped (`rounded-full`), `primary` background with `on_primary` text. Use for "Post Poem."
- **Secondary:** Capsule-shaped, `outline` border (Ghost Border style) with `on_surface` text.
- **Tertiary:** No container, `primary` text color, used for "See More."

### Poetry Cards
- **Construction:** Use `surface_container_highest` for the card body. 
- **Radius:** Always use `xl` (3rem) for cards to lean into the Spotify-inspired "liquid" friendliness.
- **Rule:** No dividers. Use `Spacing-8` (2.75rem) to separate cards.

### The "Stanza" Input Field
- **Style:** A borderless text area. Use `headline-sm` for the input text. 
- **Active State:** The cursor should be `primary` (#57f47f). The background should subtly transition to `surface_bright` when focused.

### Immersive Playback Bar (Audio Poetry)
- **Style:** Glassmorphic (`surface_variant` @ 70% + backdrop blur).
- **Radius:** `lg` (2rem).
- **Positioning:** Floating 1.4rem (`Spacing-4`) from the bottom of the screen, never docked to the edges.

---

## 6. Do’s and Don'ts

### Do:
- **Use "Breathing Room":** Use `Spacing-12` (4rem) for top-of-page margins to let the poetry breathe.
- **Embrace Asymmetry:** Align poem titles to the left, but place "Like" counts or "Author" metadata on the far right of the following line.
- **Contextual Gradients:** Use the `primary_dim` color as a soft, radial background glow (10% opacity) behind featured poems.

### Don't:
- **Don't use Dividers:** Never use a horizontal line to separate comments or poems. Use a background shift to `surface_container_low`.
- **Don't use Pure White for Body:** Use `on_surface_variant` for long stanzas to reduce eye strain in dark mode; reserve pure white for titles.
- **Don't use Sharp Corners:** Even the smallest "selection chip" must have at least a `sm` (0.5rem) radius. Sharp corners break the "Velvet Anthology" feel.

---

## 7. Spacing & Rhythm
The system uses a non-linear spacing scale to encourage "Editorial White Space."
- **Standard Padding:** `Spacing-4` (1.4rem) for internal container padding.
- **Section Gaps:** `Spacing-10` (3.5rem) to create clear mental breaks between different poets or categories.
- **Tight Metadata:** `Spacing-1.5` (0.5rem) for grouping a poet's name with their handle.```