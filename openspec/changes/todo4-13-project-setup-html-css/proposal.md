## Why

The Todo HTML App v3 needs a foundational HTML file before any features can be built. This establishes the document structure, theming system (CSS custom properties), and layout that all subsequent tickets will build upon. Without this base, no UI work can proceed.

## What Changes

- Create `index.html` with complete HTML5 document structure
- Add CSS reset (box-sizing, margin/padding normalization, system font stack)
- Define 13 CSS custom properties on `:root` for colors, spacing, border-radius, and shadow
- Build centered app container layout (max-width 600px) with semantic header, main, and footer sections

## Capabilities

### New Capabilities
- `html-structure`: HTML5 document skeleton with head meta tags, semantic body sections (header, main, footer), and app container
- `css-theming`: CSS reset, custom properties for colors/spacing/radius/shadow, and base styles applied to the document
- `responsive-layout`: Centered 600px max-width container that adapts fluidly to smaller viewports without horizontal scroll

### Modified Capabilities

None — this is the initial project setup.

## Impact

- **New file**: `index.html` (the only application file)
- **No dependencies**: zero external requests, no CDN, no build tools
- **Foundation**: all future features (todo CRUD, filtering, localStorage) will build inside this structure
