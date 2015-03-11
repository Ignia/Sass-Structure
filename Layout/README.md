# Layout Directory

The `/Layout` directory represents all of the structural components of a website: dimensions, floats, padding, margins, positioning, and responsive design breakpoints. By separating these from style-related selectors, we allow the layout to be easily managed independent of the theme.

In most sites, the `_layout.scss` file will be suitable; in large sites, however, developers may prefer to break out particular sections of the layout, such as `_header.scss`, `_footer.scss`, `_navigation.scss`, etc.; in these scenarios, these files should be placed directly into the `/Layout` directory and imported at the top of the `_layout.scss` file.

In some cases, a site may require multiple distinct layouts. For these cases, each layout should be created in a folder underneath `/Layout`. It may be advantageous to compile these independent of the main `/Manifest.scss` so they can be targeted specifically without the need for namespacing selectors, similar to `Themes`.



