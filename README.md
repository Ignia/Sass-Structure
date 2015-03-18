# Ignia Sass Structure
The projects Ignia works on come in a variety of sizes. For that reason, it is important that our Sass directory structure be comprehensive enough to accommodate large projects, without adding unnecessary complexity and overhead to small projects. To this end, we have aimed to establish a baseline structure that requires *relatively* few files, as well as a road map for how to extend that structure as projects (inevitably) grow.

## Contents
- [Variables](#variables)
- [Directories](#directories)
- [Import Strategy](#import-strategy)
- [Styles Included](#styles-included)
- [Motivation](#motivation)
  - [Emergent Trends](#emergent-trends)
    - [Ambiguous Identifiers](#ambiguous-identifiers)
  - [Acknowledgements](#acknowledgements)

## What is Sass?
Briefly, [Sass](http://sass-lang.com/) extends the syntax for Cascading Style Sheets (CSS) to allow for variables, conditions, calculations, includes, functions, and other programmatic capabilities. In effect, this greatly simplifies the process of writing CSS, reduces repetition of values, and makes stylesheets easier to maintain. Because Sass is precompiled into standard CSS, it introduces no compatibility issues.

## Variables
Ignia places the `_variables.scss` file in the root as, ideally, that is the first stop for maintaining a site's styles after it has been built. For more invasive updates, such as redesigns, developers will certainly need to modify other files, but any variables we *expect* to be modified will be in this location. Some developers place the `_variables.scss` in `/Base` or `/Helpers`; Ignia, however, maintains that this file should be immediately obvious and accessible when opening the `/Styles` directory.

> *Important:* Variables defined in other files should always use the `!default` flag so they can be *overwritten* by `_variables.scss` without *relying* on it.

## Directories
- [x] [Base](./Base/)
- [x] [Components](./Components/)
  - [ ] [ComponentA](./Components/ComponentA/)
- [ ] [Global](./Global/)
  - [ ] [Defaults](./Global/Defaults/)
  - [ ] [Admin](./Global/Admin/)
  - [ ] [Helpers](./Global/Helpers/)
- [x] [Helpers](./Helpers/)
- [x] [Layout](./Layout/)
- [x] [Overrides](./Overrides/)
- [ ] [Themes](./Themes/)
  - [ ] [Brand](./Themes/Brand/)
  - [ ] [Theme](./Themes/Theme/)
- [x] [Vendor](./Vendor/)
- [x] [Views](./Views/)

> *Note:* Checked items are considered default directories and should always be maintained, if only as placeholders; unchecked items are either optional or only provided as sample content.

## Import Strategy
To support a variety of project sizes, some concepts that are typically kept distinct in large projects (such as variables, manifests, and styles) may be consolidated in smaller projects. For example, every directory (including the root) has a file with the same name as the parent directory; e.g., the `/Base` directory contains a file named `_base.scss`. For a small site, this file may contain all base styles; for a larger site, however, it will be used *exclusively* as a manifest (i.e., responsible for importing all other files in the `/Base` directory). Regardless of a site's state of growth, however, authors have the assurance that all dependencies can be imported into the `/Style.scss` file by simply importing the `/Directory/_directory.scss` file.

> *Note:* The `/Themes` and `/Views` folders may not have manifest files (e.g., `/Themes/_theme.scss`) as it is recommended that these styles be compiled independent from the centralized CSS file. For more information, see the [Themes Directory documentation](./Themes/).

## Styles Included
The goal of this project is to establish a baseline file and directory structure, not to provide a "UI framework". As such, the Sass files contain a minimal amount of markup. Nonetheless, we have provided a handful of styles in order to help demonstrate the approach and provide boilerplate reference. Where possible, we've only done this with styles that we expect most sites will want to override (i.e., variables like `font-family` and `font-size` in `/Base/_base.scss`).

## Motivation

### Emergent Trends
In developing our Sass structure we aimed to identify emerging trends in how other developers are structuring their Sass projects, instead of relying exclusively on our own internal conventions. This is important since Ignia works with many contractors, partners, and client developers. To this end, we've leveraged commonly used naming conventions such as `/Base`, `/Components`, `/Helpers`, `/Layouts`, `/Vendor`, and `/Views`.

#### Ambiguous Identifiers
Despite the above, there are a number of popular identifiers that Ignia chose not to use. These include, for instance, `/Modules`, `/Partials`, and `/Utilities`. While Ignia has our own consistent definition for each of these terms, we found that their definitions vary considerably across Sass implementations and are thus ambiguous means of organizing content. For instance, `/Utilities` sometimes refer to CSS utility classes (e.g., `.clearfix`), while other times it refers to Sass utilities (e.g., functions, mixins, and placeholders).

### Acknowledgements
In developing our Sass directory structure, Ignia relied heavily on best practices established by the broader web development community. In particular, each of the following articles played an influence in some of the conventions we have adopted.
- [Clean Out Your Sass Junk-Drawer](http://gist.io/4436524) by [Dale Sande](https://github.com/anotheruiguy)
- [Architecture for a Sass Project](http://www.sitepoint.com/architecture-sass-project/) by [Hugo Giraudel](https://github.com/HugoGiraudel)
- [How to Structure a Sass Project](http://thesassway.com/beginner/how-to-structure-a-sass-project) by [John W. Long](http://wiseheartdesign.com/)
- [Scalable and Modular Architecture for CSS](https://smacss.com/) by [Jonathan Snook](https://github.com/snookca)

<small>*Ignia is a registered trademark of Ignia, LLC.*</small>
