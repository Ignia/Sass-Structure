# Themes Directory

In some cases, a site may have multiple themes, which may be selectable by content owners (e.g., for a blog) or even end users (e.g., many web-based mail clients offer user-selectable themes). In these cases, themes should be placed within the `/Themes` folder.

Typically, themes will involve multiple files, and thus each theme should live in its own subdirectory. A specialized version of a theme is a global brand default that is used across multiple sites; that may also live in the `/Themes` folder.

## Targeting
It is important to note that there is manifest file for `/Themes` (i.e., no `_themes.scss`). It is Ignia’s strong opinion that themes should be compiled independently of the main stylesheet and included dynamically (ideally by the server). As an alternative, some developers may wish to namespace their themes by placing a class name on, for instance, the body element. Ignia advises against this strategy as it bloats the CSS code (i.e., all themes must be included, even though only one is used at a time) and requires increased specificity of selectors (e.g., to overwrite a theme-specific style, the selector must also include the theme’s class name).

