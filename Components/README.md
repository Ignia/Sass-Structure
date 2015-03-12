# Components Directory

Components represent reusable blocks that are expected to be applied multiple times across a site. From a CSS perspective, these require coordination of multiple styles (often classes) to achieve a unified output—although in methodologies such as [BEM](https://en.bem.info/) or [FUN](http://benfrain.com/fun-css-naming-convention-explained/), these may be composited together to reduce specificity.

> *Note:* Ignia does not use BEM or FUN naming conventions, but the Sass structure is intended to be naming convention agnostic.

# Naming
From Ignia’s perspective, components will frequently map to other blocks of reusable code, such as an MVC partial, an AngularJS directive, or a JavaScript control (such as a Date Picker); in those cases, the component should share the same name as their counterparts (e.g., `Menu.js` would map to `/Components/Menu/_menu.scss`).

# Scaling
Because the goal of components is to encapsulate functionality, SCSS components may have their own placeholders (via `_placeholders.scss`), functions (via `_functions.scss`), and mixins (via `_mixins.scss`); all of these will be assembled in a `/Component/Component/_component.scss` file (e.g., `/Components/Menu/_menu.scss`). Each component will be imported into the `_components.scss` file so they are easy to reference.

