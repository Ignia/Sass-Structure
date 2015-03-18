# Base Directory

The `/Base` directory targets default site styling for standard HTML elements, and typically uses selectors that target elements (e.g., `h1`, `input`), attributes (e.g., `[type='submit']`), and/or singular class declarations (e.g., `.error`, `.required`).

## Files
It is expected that all projects will need to, at minimum, define:
- Importing of web fonts (via `_fonts.scss`),
- Overrides for standard type settings (e.g., `h1`-`h6`, via `_typography.scss`),
- Form elements (e.g., `input[type="text"]` via `_forms.scss`), and
- Utility selectors for commonly-used style applications (e.g., `.centered`, via `_utilities.scss`).

Other overrides may optionally stay in the `_base.scss` file.

## Scaling
For large projects, additional overrides should be broken out into their own files (e.g., `_lists.scss`, `_tables.scss`, etc.) as needed. When doing so, these partials should be included in `_base.scss` via an `@import` statement at the top of the file.

