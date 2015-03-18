# Views Directory

While it’s a practice Ignia aims to avoid, some CSS styles are invariably going to be page-specific and can’t be abstracted into, for example, components. For instance, homepages frequently break design rules implemented elsewhere on the site. In these cases, view-specific stylesheets become necessary.

## Files
All styles should be placed in a file named after the view (in MVC terms) and/or page they are modifying. For instance, assuming a corresponding view is `Home.html`, styles for the homepage may be placed in a `Home.scss` page.

## Compilation
Ideally, view-specific styles should be compiled independently and imported *exclusively* by their corresponding view. This ensures that page-specific views don't bloat the centralized CSS file. In some situations, however, it may be preferable to centralize these (for instance, when these changes are very small, and carefully namespaced). In those cases, view-specific overrides are placed in the `/Views` directory, use the partial naming convention (e.g., `_home.scss`), and are imported via the `_views.scss` file.

> *Note:* No view-specific styles should be placed in the `_views.scss` file; *if* used, this should *only* include `@import` statements.
