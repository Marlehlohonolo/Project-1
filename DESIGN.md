# Design System Document: The Editorial Sanctuary

## 1. Overview & Creative North Star
### Creative North Star: "The Digital Hearth"
This design system moves away from the sterile, transactional nature of traditional non-profit sites. Instead, it adopts an **Editorial Sanctuary** aesthetic—combining the authority of a high-end publication with the tactile warmth of a community home. 

We break the "template" look through **intentional asymmetry** and **tonal depth**. Instead of rigid grids, we use overlapping elements (e.g., an image bleeding into a text block) and expansive white space to create a sense of breathing room and calm. The goal is to move the donor from a state of "processing data" to a state of "feeling connection."

---

## 2. Colors & Surface Philosophy
The palette balances the reliability of soft teals (`primary`, `secondary`) with the urgent warmth of oranges (`tertiary`).

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section content. Boundaries must be defined solely through:
1.  **Background Color Shifts:** Use `surface-container-low` sections sitting on a `surface` background.
2.  **Tonal Transitions:** A subtle shift from `surface` to `surface-variant` creates a natural break without the "boxed-in" feel of a stroke.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine cotton paper.
*   **Base:** `surface` (#faf9f8) for the main page body.
*   **Layer 1:** `surface-container-low` (#f4f3f2) for large content sections (e.g., the "Our Mission" section).
*   **Layer 2 (The Card):** `surface-container-lowest` (#ffffff) for interactive cards or donation modules to provide a soft, natural lift.

### The "Glass & Gradient" Rule
To elevate the experience beyond "flat design," use **Glassmorphism** for floating elements (like sticky navigation or donate FABs) using `surface` at 80% opacity with a `20px` backdrop-blur. 
*   **Signature Texture:** Use a linear gradient from `primary` (#006474) to `primary-container` (#2d7d8e) on main CTAs to add "soul" and professional polish.

---

## 3. Typography: The Editorial Voice
We use a high-contrast scale to create an authoritative yet inviting hierarchy.

*   **Display & Headlines (Newsreader):** This friendly serif brings a human, "storytelling" quality. Use `display-lg` (3.5rem) for hero statements to command attention without shouting.
*   **Titles & Body (Manrope):** A clean, modern sans-serif that ensures high legibility for complex information (e.g., financial transparency reports).
*   **The Identity Mix:** Always pair a `headline-md` (Newsreader) with a `body-lg` (Manrope) lead-in paragraph. This contrast signals that the content is both professional (sans) and heart-centered (serif).

---

## 4. Elevation & Depth
We eschew traditional shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` background. This creates "soft lift" that feels organic to the environment.
*   **Ambient Shadows:** If an element must float (e.g., a modal), use a shadow color tinted with `on-surface` at 6% opacity with a `40px` blur. Avoid "drop shadows" that look like dark grey stains.
*   **The Ghost Border Fallback:** If accessibility requires a border, use `outline-variant` (#bec8cb) at **15% opacity**. This provides a "suggestion" of a boundary rather than a hard wall.

---

## 5. Components

### Buttons
*   **Primary:** Background: Gradient (`primary` to `primary-container`). Text: `on-primary`. Shape: `md` (0.75rem) roundedness. 
*   **Secondary:** Background: `secondary-container`. Text: `on-secondary-container`. 
*   **Tertiary (The "Warmth" Action):** Background: `tertiary`. Used sparingly for "Urgent Needs" or "Donate Now."

### Cards & Lists
*   **The "No Divider" Rule:** Forbid the use of 1px divider lines. Separate list items using `spacing-4` (1.4rem) of vertical white space or by alternating background tones between `surface-container-low` and `surface-container-lowest`.
*   **Donation Tiers:** Use `xl` (1.5rem) rounded corners for donation amount cards to make them feel exceptionally "soft" and inviting.

### Input Fields
*   **Text Inputs:** Background should be `surface-container-highest` (#e3e2e1) with no border. On focus, transition to a `2px` underline of `primary`.
*   **Labels:** Always use `label-md` in `on-surface-variant`.

### Signature Component: The Impact Progressor
A custom progress bar for fundraising goals using a thick `12px` track in `secondary-fixed-dim` with a `secondary` fill. The roundedness is `full` to evoke a "pill" shape that feels modern and approachable.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Offset images by `spacing-8` (2.75rem) from the text container to create an editorial layout.
*   **Use Large Spacing:** Lean into `spacing-16` (5.5rem) and `spacing-20` (7rem) between major sections to let the "hopeful" teal palette breathe.
*   **Micro-copy Matters:** Use `label-sm` for tiny supportive text (e.g., "Your $50 provides 3 meals").

### Don't:
*   **No Hard Edges:** Never use `none` (0px) roundedness. It breaks the "community-focused" warmth.
*   **No Pure Black:** Never use #000000. Use `on-background` (#1a1c1c) for text to maintain a soft, ink-on-paper look.
*   **No Crowding:** If a section feels "busy," increase the background tonal contrast instead of adding lines or boxes.