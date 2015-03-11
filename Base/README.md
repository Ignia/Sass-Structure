# Base Directory

The `/Base` directory targets default browser styling for standard HTML elements, and typically uses selectors that target elements, attributes, and/or singular class declarations. It is expected that projects will need to import fonts (via `_fonts.scss`), override standard type settings (e.g., `h1`-`h6`, via `_typography.scss`), and form elements (e.g., `input[type="text"]` via `_forms.scss`). Other overrides may optionally stay in the `_base.scss` file, although on large projects, these can be broken out into their own files (e.g., `_lists.scss`, `_tables.scss`, etc.) as needed. When doing so, these partials should be included in `_base.scss` via an `@import` statement at the top of the file.

