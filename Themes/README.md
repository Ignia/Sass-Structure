# Themes Directory

In some cases, a site may have multiple themes, which may be selectable by content owners (e.g., for a blog) or even end users (e.g., many web-based mail clients offer user-selectable themes). In these cases, themes should be placed within the `/Themes` folder.

> A specialized version of a theme is a global brand default that is used across multiple sites. If this is specific to a project (e.g., it belongs to a customer) then it should live under the `/Themes` folder; if it is global to the organization, it should live in the `/Global/Themes/` folder.

## Files
Typically, themes will involve multiple files, and thus each theme should live in its own subdirectory. E.g., a theme called "Admin" will live in a `/Themes/Admin/` folder, and expose a manifest at `/Themes/Admin/_admin.scss`.

## Compilation
Themes should be compiled independently of the main stylesheet and included dynamically (ideally by the server). For this reason, there is not a manifest file for the `/Themes` folder (i.e., no `_themes.scss`). As an alternative, some developers may wish to namespace their themes by placing a class name on, for instance, the `body` element. Ignia advises against this strategy as it bloats the CSS code (i.e., all themes must be included, even though only one is used at a time) and requires increased specificity of selectors (e.g., to overwrite a theme-specific style, the selector must also include the theme’s class name).

