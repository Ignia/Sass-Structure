# Views Directory

While it’s a practice we try to avoid, the reality is that some CSS styles are page-specific and can’t be abstracted into, for example, components. For instance, homepages frequently break design rules implemented elsewhere on the site. In these cases, view specific stylesheets become necessary.

Ideally, Ignia prefers to keep view-specific styles tied to the views they represent (e.g., alongside a `_view.html` in an MVC application), and compile them as separate CSS files so that these page-specific views aren’t bloating the centralized CSS file. In some situations, however, it is preferable to centralize these (for instance, when these changes are very small, and carefully namespaced). In those cases, view-specific overrides are placed in the `/Views` directory, named `_view.scss`, and imported via the `_views.scss` file.

