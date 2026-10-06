# Change 2: Clarify the current page in navigation

## Goal

Make it immediately clear which portfolio page a visitor is viewing while keeping the site's existing visual style consistent.

## What we plan to change

- Refine the visual active state for the existing Home, About, Experience, and Contact links so the current page stands out more clearly on desktop and mobile.
- Keep the existing `aria-current="page"` semantics and ensure the visual state matches the current page.
- Preserve the current navigation structure, typography, colors, spacing, responsive behavior, and keyboard focus styling.

## Why this improves usability and navigation

- Visitors can identify their location in the portfolio at a glance.
- A clearer current-page state makes it easier to navigate between sections without losing context.
- Keeping the indicator consistent with the existing visual style and accessible page-state semantics supports both visual and assistive-technology users.
