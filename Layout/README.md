# Layout Directory

The `/Layout` directory represents all of the structural components of a website: dimensions, floats, padding, margins, positioning, and responsive design breakpoints. By separating these from style-related selectors, we allow the layout to be easily managed independent of the theme.

> *Note:* The `/Layout` directory is the *only* location where ID-based selectors (e.g., `#identifier`) are expected to appear. These *may* be appropriate since layout sections (e.g., header, footer, navigation) are only expected to occur once on any given page. They should be used with caution since they tie the style to specific structure components and increase specificity.

## Files
In most sites, the `_layout.scss` file will be suitable. In complex sites, however, developers may prefer to break out particular sections of the layout, such as:
- `_header.scss`
- `_footer.scss`
- `_navigation.scss`
- etc.

In these scenarios, these files should be placed directly into the `/Layout` directory and imported at the top of the `_layout.scss` file.

## Scaling
Many sites will only have a single layout, with exceptions being handled under `/Views`. In some cases, however, a site may require multiple distinct layouts. In this scenario, each layout should be created in a file underneath `/Layout`. These layouts may only require a single file (e.g., `_threePane.scss`); if multiple files are needed, these should be placed in a subfolder (e.g., `/Layout/ThreePane/`).

> *Note:* It may be advantageous to compile these independent of the main `Style.scss` so they can be targeted specifically without the need for namespacing selectors. In this scenario, individual layouts should not be imported into the `_layout.scss` file. This is discussed in more detail under [Themes](./Themes/Readme.md).
