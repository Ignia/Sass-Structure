# Helpers Directory

Helpers provide, exclusively, functional code that does not output style declarations directly. They are intended to aid in the assembly of stylesheets. This may include, for instance, reusable mixins or functions.

## Files
Helper files should be broken down by type, so their function is clear and they're easy to find. This includes:
- Placeholders (in `_placeholders.scss`),
- Mixins (in `_mixins.scss`), and
- Functions (in `_functions.scss`).

## Scaling
For a large site, it may be preferable to break these files down into smaller components. In this case, it is recommended that partials be created in associated subfolders (e.g., `/Helpers/Mixins/`), with helpers distributed amongst individual partials (e.g., `_colors.scss`). In this case, the associated manifest (e.g., `_mixins.scss`) should be moved into that subdirectory.

> *Note:* For Ignia, it is expected that many mixins and functions, at least, will be of value beyond any single project, and thus will frequently be centralized in the `/Global/Helpers/` directory. Given this, a single file is typically enough granularity for most projects.

