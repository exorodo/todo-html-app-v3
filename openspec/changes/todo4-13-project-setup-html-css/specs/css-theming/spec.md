## ADDED Requirements

### Requirement: CSS reset applied
The document SHALL apply box-sizing: border-box to all elements (*, *::before, *::after), remove default margin and padding on body, set a system font stack, and enable antialiased font rendering.

#### Scenario: Box-sizing is border-box globally
- **WHEN** a developer inspects any element
- **THEN** its computed box-sizing is border-box

#### Scenario: Body has no default margin or padding
- **WHEN** a developer inspects the body element
- **THEN** margin and padding are both 0

### Requirement: CSS custom properties defined on :root
The `:root` selector SHALL define the following custom properties: --color-primary (#4a90d9), --color-bg (#f5f5f5), --color-surface (#ffffff), --color-text (#333333), --color-text-secondary (#666666), --color-border (#e0e0e0), --color-danger (#e74c3c), --color-success (#27ae60), --spacing-sm (0.5rem), --spacing-md (1rem), --spacing-lg (1.5rem), --radius (8px), --shadow (0 2px 8px rgba(0,0,0,0.1)).

#### Scenario: All custom properties are available
- **WHEN** a developer inspects :root custom properties
- **THEN** all 13 custom properties are defined with their specified values

### Requirement: Base styles use custom properties
The body background, text color, and app container styles SHALL reference CSS custom properties rather than hard-coded values.

#### Scenario: Styles reference custom properties
- **WHEN** a developer inspects the CSS source
- **THEN** body background uses var(--color-bg), text uses var(--color-text), and the app container uses var(--color-surface) and var(--shadow)
