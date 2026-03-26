## ADDED Requirements

### Requirement: Centered app container
The `#app` container SHALL have a max-width of 600px with auto horizontal margins, padding using spacing custom properties, and a white background with subtle shadow.

#### Scenario: Container is centered at desktop width
- **WHEN** a user opens index.html on a viewport wider than 600px
- **THEN** the app container is horizontally centered with white background and shadow

### Requirement: Fluid responsive behavior
The layout SHALL adapt fluidly to viewports smaller than 600px without producing horizontal scroll. Body SHALL have min-height: 100vh.

#### Scenario: No horizontal scroll on mobile
- **WHEN** a user resizes the browser window below 600px
- **THEN** the container fills the available width with consistent padding and no horizontal scrollbar appears

#### Scenario: Full viewport height
- **WHEN** a user opens the page with minimal content
- **THEN** the body fills the full viewport height (min-height: 100vh) with the background color
