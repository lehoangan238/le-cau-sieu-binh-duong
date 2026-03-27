# Design System Document: The Sacred Horizon

## 1. Overview & Creative North Star
**Creative North Star: "The Ethereal Sanctuary"**

This design system is crafted to honor the profound solemnity of the *Đại lễ Cầu siêu - Cầu An Tiết Thanh Minh 2026*. Moving away from the rigid, boxy constraints of traditional web design, "The Ethereal Sanctuary" focuses on a high-end editorial experience that mimics the serenity of a Buddhist temple at dawn. 

We break the "template" look by utilizing **intentional asymmetry**—allowing imagery and typography to breathe and overlap—creating a sense of organic flow. The experience is not just a digital interface; it is a curated journey of peace and remembrance. By leveraging vast whitespace, sophisticated tonal layering, and "glowing" focal points, we ensure the UI feels premium, intentional, and deeply respectful.

---

## 2. Colors & Atmospheric Depth
The palette is rooted in the earth and the divine, utilizing a sophisticated Material 3-based tonal range to create warmth without clutter.

### Color Tokens
- **Primary (The Divine):** `primary` (#735C00) & `primary_container` (#D4AF37). Use these for moments of enlightenment and primary actions.
- **Secondary (The Earth):** `secondary` (#765749) & `on_secondary_fixed_variant` (#5C4033). Represents the grounding presence of wood and tradition.
- **Tertiary (The Compassion):** `tertiary` (#AC2471). A refined Lotus Pink used sparingly for emotional highlights or soft accents.
- **Neutral (The Void):** `background` (#FBF9F5) and its surface variants.

### The "No-Line" Rule
To maintain a "peaceful and clean" aesthetic, **1px solid borders are strictly prohibited** for sectioning or containment. Boundaries must be defined through:
1.  **Background Color Shifts:** Transitioning from `surface` to `surface_container_low`.
2.  **Negative Space:** Using the Spacing Scale to create natural "islands" of content.

### The Glass & Gradient Rule
To achieve a "premium" feel, floating navigation elements or modal overlays must utilize **Glassmorphism**. Use `surface_container_lowest` at 80% opacity with a `20px` backdrop-blur. 
**Signature Gradients:** For Hero backgrounds or high-level CTAs, use a subtle radial gradient: `primary_container` (#D4AF37) fading into a transparent `surface` to create a "glowing" effect rather than a flat block of color.

---

## 3. Typography: The Editorial Voice
The typography is a dialogue between the timeless (Serif) and the modern (Sans-Serif).

| Level | Token | Font | Size | Intent |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Playfair Display | 3.5rem | For mantras or core event titles. |
| **Headline** | `headline-md` | Playfair Display | 1.75rem | Section headers; conveys solemnity. |
| **Title** | `title-lg` | Inter | 1.375rem | Information architecture; modern and clear. |
| **Body** | `body-lg` | Inter | 1rem | Primary reading experience; high legibility. |
| **Label** | `label-md` | Inter | 0.75rem | Meta-data, dates, and small captions. |

**Styling Note:** Display and Headline text should use a slightly tighter letter-spacing (-0.02em) to feel "custom-set," while Body text should use increased line-height (1.6) to promote a peaceful reading pace.

---

## 4. Elevation & Tonal Layering
We do not use shadows to create "pop"; we use them to create "atmosphere."

*   **The Layering Principle:** Stack surfaces to create depth. A card using `surface_container_lowest` (white-adjacent) should sit on a `surface_container` (light grey/cream) background. This creates a soft, natural lift.
*   **Ambient Shadows:** If a floating element is required, use a shadow with a 40px blur and 4% opacity, using the `on_surface` color as the shadow base. It should feel like a soft glow, not a dark drop-shadow.
*   **The Ghost Border:** For form inputs or necessary boundaries, use `outline_variant` (#D0C5AF) at **15% opacity**. This provides a "suggestion" of a container without breaking the visual calm.

---

## 5. Components & Primitive Logic

### Buttons (The Path to Action)
*   **Primary:** A "Glow" button. Background: `primary_container` (#D4AF37). No border. Soft `sm` (0.125rem) roundedness to keep it architectural and sharp, not "bubbly."
*   **Secondary:** Ghost style. No background. `primary` text. Upon hover, a subtle `surface_container_high` background appears.

### Cards (The Content Vessels)
*   **Rule:** No dividers. Separate content using `spacing-6` (2rem) of vertical space.
*   **Visuals:** Cards should feature a subtle lotus watermark in the bottom-right corner using a 5% opacity `primary` tint.

### Input Fields (The Offering)
*   **Style:** Minimalist. No background fill. Only a bottom "Ghost Border" using `outline_variant`.
*   **States:** On focus, the bottom border transitions to `primary` (#735C00) with a subtle 2px thickness.

### Signature Component: The "Zen Scroll"
A vertical progress indicator for long-form event descriptions, using a thin `primary_container` line that "grows" as the user scrolls, capped with a small, glowing lotus icon.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Place an image of a lotus ceremony off-center, allowing the `display-lg` text to overlap the edge of the image.
*   **Use High-Quality Imagery:** Ensure photos have a warm temperature, emphasizing gold leaf, candle-light, and soft morning mist.
*   **Prioritize Breathing Room:** Use `spacing-16` (5.5rem) or `spacing-20` (7rem) between major sections to let the mind rest.

### Don’t:
*   **Don’t use "Pure Black":** Use `on_surface` (#1B1C1A) for text to keep the contrast soft and "warm."
*   **Don’t use vibrant Pink (#FF69B4) as a primary background:** Use it only for delicate accents—like a notification dot or a "heart" icon for prayers.
*   **Don’t use heavy rounding:** Keep roundedness to `sm` or `none` for a more architectural, premium, and "temple-like" structure. Reserve `full` only for small chips or tags.

### Final Director's Note:
*Remember: Every pixel should feel like an act of mindfulness. If a layout feels "busy," remove an element. If it feels "cold," increase the warmth of the surface-container tokens.*