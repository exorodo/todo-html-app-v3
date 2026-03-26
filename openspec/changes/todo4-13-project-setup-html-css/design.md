## Context

This is a greenfield project — no existing code. The Todo HTML App v3 is a single-file vanilla HTML/CSS/JS application with no build tools or external dependencies. All markup, styles, and scripts live in one `index.html`.

## Goals / Non-Goals

**Goals:**
- Establish a valid HTML5 document with semantic structure
- Create a reusable CSS theming system via custom properties
- Provide a centered, responsive app container ready for feature development

**Non-Goals:**
- No JavaScript functionality (handled by future tickets)
- No todo list UI elements yet
- No dark mode or theme switching
- No external CSS frameworks or resets (e.g., normalize.css)

## Decisions

**Single-file architecture**: All CSS is inline in a `<style>` tag within `<head>`. This keeps the app zero-dependency and instantly loadable — no HTTP requests beyond the HTML file itself.

**CSS custom properties over Sass/variables**: Custom properties work natively in all modern browsers, can be overridden at runtime (enabling future dark mode), and require no build step.

**System font stack**: Using `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif` avoids font loading delays and matches the user's OS aesthetic.

**Semantic HTML (header/main/footer)**: Provides accessibility landmarks for screen readers and a clear document outline without extra ARIA roles.

## Risks / Trade-offs

**Single-file scaling** — as features are added, `index.html` will grow. For a small todo app this is acceptable; a larger app would need splitting. → Mitigated by keeping CSS organized with comments and using custom properties for consistency.

**No CSS reset library** — minimal hand-written reset covers box-sizing and body margin only. Some elements (lists, buttons) may need per-feature normalization. → Acceptable for this scope; future tickets handle those elements.
