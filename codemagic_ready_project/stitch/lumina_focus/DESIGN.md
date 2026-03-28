# Design System Document: The Focused Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Sanctuary."** 

In a world of cluttered productivity tools, this system rejects the "dashboard" aesthetic in favor of a high-end editorial experience. We move beyond generic utility by using intentional asymmetry, expansive whitespace, and sophisticated tonal layering. The goal is to make "tracking" feel less like a chore and more like a mindful ritual. By utilizing the 'Abu Jm Akkas' typeface alongside modern sans-serifs, we create a bridge between heritage and high-tech efficiency.

## 2. Colors & Surface Architecture
We move away from the "boxed-in" look of traditional apps. Our palette is rooted in a professional Deep Teal (`primary`) and a growth-oriented Forest Green (`secondary`).

### The "No-Line" Rule
**Strict Mandate:** Prohibit the use of 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. Use `surface-container-low` for secondary sections sitting on a `surface` background. This creates a "soft-edge" layout that feels fluid rather than rigid.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine vellum. 
- **Base Layer:** `surface` (#f6fafa)
- **Secondary Content:** `surface-container-low` (#f1f4f4)
- **Interactive Components:** `surface-container-lowest` (#ffffff) to create a subtle lift.
- **Elevation Peak:** For high-priority modals, use `surface-bright` with a backdrop blur.

### The "Glass & Gradient" Rule
To inject "soul" into the interface:
- **CTAs:** Use a subtle linear gradient from `primary` (#006067) to `primary_container` (#007b83) at a 135-degree angle.
- **Floating Elements:** Use `surface_container_lowest` at 85% opacity with a `20px` backdrop-blur to create a "frosted glass" effect.

## 3. Typography: Editorial Authority
The typography system balances the precision of *Plus Jakarta Sans* with the cultural character of *Abu Jm Akkas*.

| Role | Font Family | Size | Intent |
| :--- | :--- | :--- | :--- |
| **Display-LG** | Plus Jakarta Sans | 3.5rem | High-impact hero stats. |
| **Headline-LG** | Abu Jm Akkas | 2.0rem | Primary Page Headers (Bangla & English). |
| **Title-MD** | Plus Jakarta Sans | 1.125rem | Task names and Card headers. |
| **Body-MD** | Abu Jm Akkas / Jakarta | 0.875rem | Descriptions and long-form notes. |
| **Label-SM** | Plus Jakarta Sans | 0.6875rem | Metadata and Micro-copy. |

*Director's Note:* Use `headline-lg` in Abu Jm Akkas for a signature look that feels custom-built for the user's language and context.

## 4. Elevation & Depth
We achieve hierarchy through **Tonal Layering** rather than shadows or lines.

- **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` card on a `surface-container-low` background. The contrast in "cleanliness" provides the lift.
- **Ambient Shadows:** Only for floating elements (FABs, Modals). Use `on-surface` color at 6% opacity with a `32px` blur and `8px` Y-offset. This mimics natural light rather than a "computer-generated" drop shadow.
- **The Ghost Border:** If accessibility requires a stroke, use `outline-variant` (#bdc9ca) at **15% opacity**. It should be felt, not seen.

## 5. Components

### Developer Identity Card
A signature component placed within the 'About' or 'Profile' sections.
- **Container:** `surface-container-lowest`, `xl` (1.5rem) corner radius.
- **Image:** {{DATA:IMAGE:IMAGE_1}} masked in a soft-squircle.
- **Layout:** Asymmetric. Image flush to the left, typography right-aligned with `primary` color accents for the developer name.
- **Visual Flourish:** A `secondary_container` glow behind the profile image at 20% opacity.

### Buttons & Inputs
- **Primary Button:** `xl` (1.5rem) roundedness. No border. Gradient fill (`primary` to `primary_container`).
- **Secondary/Success Button:** `secondary_fixed` (#94f990) background with `on_secondary_fixed` text. Used for "Prayer Complete" or "Goal Met" states.
- **Input Fields:** `surface-container-highest` background. No border. On focus, transition the background to `surface_container_lowest` with a `ghost border` of `primary`.

### Cards & Lists
- **Forbid Dividers:** Never use a horizontal line to separate list items. Use `spacing-4` (1.4rem) of vertical whitespace or alternating subtle tints of `surface-container-low`.
- **Chips:** Use `lg` (1rem) roundedness. `primary_fixed` background for active filters to maintain vibrancy without heavy weight.

## 6. Do's and Don'ts

### Do
- **Embrace Whitespace:** If it feels "too empty," you are likely on the right track. Use the `20` (7rem) spacing scale for major section breathing room.
- **Asymmetric Balance:** Align headers to the left but allow secondary data to float or align right to create a dynamic, editorial feel.
- **Tone-on-Tone:** Use `on_surface_variant` for secondary text to keep the UI soft and approachable.

### Don't
- **No Pure Black:** Never use #000000. Use `on_surface` (#181c1d) for text to maintain the "sanctuary" feel.
- **No Hard Corners:** Avoid anything below the `md` (0.75rem) roundedness scale. Softness is a brand pillar.
- **No Crowding:** Do not place more than three high-level actions on a single screen. Force focus through intentional exclusion.