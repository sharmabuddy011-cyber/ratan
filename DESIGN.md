# Design System: Deep Void

## 1. Overview & Creative North Star
**Creative North Star: "The Silent Sentinel"**

This design system is an exercise in extreme restraint and high-fidelity precision. It moves away from the "noisy" aesthetics of traditional dashboards to embrace a monastic, terminal-inspired luxury. By utilizing a "Deep Void" palette, we create an environment where information doesn't just sit on a screen—it emerges from the shadows.

To break the "template" look, we employ **Command-Line Minimalism**:
- **Intentional Asymmetry:** Avoid perfectly centered layouts. Group critical data in the top-left or bottom-right clusters to mimic advanced robotics telemetry.
- **Micro-Interactions:** Every movement must be sharp and instantaneous (0-150ms).
- **The Void Effect:** High-contrast neon accents against pure black create a sense of infinite depth, suggesting a system that is always watching, always active, but never intrusive.

---

## 2. Colors & Surface Architecture
The palette is rooted in absolute darkness. We eliminate all blue-spectrum greys in favor of neutral and "warm-black" tones to maintain a premium, tactical feel.

### The Palette (Core Tokens)
- **Background:** `#131313` (The base void)
- **Surface Container Lowest:** `#0e0e0e` (Deep recessed areas)
- **Surface Container High:** `#2a2a2a` (Raised interaction zones)
- **Primary (Accent):** `#ffffff` (High-fidelity data/branding)
- **Surface Tint (Neon):** `#4ae176` (System status/critical alerts)

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To separate a sidebar from a main feed, use a shift from `surface` (`#131313`) to `surface-container-low` (`#1b1b1b`). Definition must be felt through tonal shifts, not seen through lines.

### Glass & Texture
For floating modules or "Heads-Up Display" (HUD) elements, use **Glassmorphism**:
- **Background:** `surface_container` at 60% opacity.
- **Backdrop-blur:** 20px - 40px.
- **Result:** Elements appear as "dark glass" floating over the void, maintaining the high-fidelity terminal aesthetic.

---

## 3. Typography: Space Grotesk
We utilize **Space Grotesk** for its mathematical precision and slightly eccentric apertures, which evoke a robotics/security feel.

- **Display (Large):** `3.5rem`. Used for "System Status" or "Secure" indicators. Tracked tightly (-2%).
- **Headline (Medium):** `1.75rem`. Used for "ADVISOR" modules and primary navigation headers.
- **Labels (Small/Medium):** `0.75rem`. **Always Uppercase.** This is our primary tool for the "Terminal" aesthetic. Increase letter spacing to `0.1rem` for maximum legibility and a premium feel.

**Correction Protocol:** All system text must undergo a rigorous spell-check. Terms like "ADVISOR" and "MONITORING" must be pristine. Errors break the illusion of high-end security.

---

## 4. Elevation & Depth
In the Deep Void, light is a luxury. We do not use traditional drop shadows.

### The Layering Principle
Hierarchy is achieved by "stacking" the void:
1. **The Floor:** `surface_dim` (`#131313`).
2. **The Recess:** `surface_container_lowest` (`#0e0e0e`) for input fields or code blocks.
3. **The Lift:** `surface_container_high` (`#2a2a2a`) for active cards or hover states.

### The "Ghost Border" Fallback
If accessibility requires a container edge, use the `outline_variant` (`#474747`) at **15% opacity**. It should be a suggestion of an edge, visible only when the eye seeks it.

---

## 5. Components & Primitive Styling

### Buttons: Tactical Precision
*   **Primary:** Solid `primary` (`#ffffff`) with `on_primary` (`#002109`) text. Square corners (`0px`).
*   **Secondary:** Ghost style. No background, `outline` border at 20%, text in `primary`.
*   **Action (Neon):** Use `surface_tint` (`#4ae176`) only for "Authorize" or "Secure" actions. Use sparingly.

### Inputs: Terminal Style
*   **Base:** `surface_container_lowest` background. 
*   **Active State:** A 1px bottom-border using `surface_tint` (`#4ae176`). No full-box focus rings.
*   **Typography:** All input text uses `label-md` uppercase for a data-entry feel.

### Cards & Lists: The "Seamless" Feed
*   **Rule:** Forbid all dividers.
*   **Separation:** Use `spacing-12` (2.75rem) of vertical white space to separate list items.
*   **Hover:** Shift background to `surface_container_highest` (`#353535`) with a 0ms transition for a "glitch-free" response.

### The "Sentinel" Shield Logo
*   **Header:** Scaled to 24px, pure white.
*   **Watermark:** Scaled to 400px, placed in the bottom-right corner at 3% opacity. It should be nearly invisible, appearing only on high-quality displays.

---

## 6. Do’s and Don’ts

### Do:
- **Embrace the Dark:** Use pure black backgrounds to make the neon green "pop" like a laser.
- **Square Everything:** `0px` border radius across the entire system. Roundness suggests "consumer-grade"; sharp corners suggest "industrial-grade."
- **Editorial Spacing:** Use exaggerated breathing room (Spacing 16+) to frame critical data points.

### Don’t:
- **No Blue:** Ensure no hex code contains a high blue value. The palette must remain monochromatic and green-accented.
- **No Shadows:** Traditional shadows look "muddy" on pure black. Use tonal shifts instead.
- **No Icons without Labels:** In a high-security context, ambiguity is a failure. Always pair icons with a `label-sm` text element.
- **No "Default" Transitions:** Avoid slow, easing curves. Use "Linear" or "In-Exponetial" for a robotic, snapped-in feel.