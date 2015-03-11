# Ignia SASS Structure
Ignia's internal file and directory structure for CSS pre-compiled using SASS.

## Variables
Ignia places the `_variables.scss` file in the root as, ideally, that is the first stop for maintaining the site styles after the site has been built. For more invasive updates or refreshes, developers will certainly need to modify other directories, but any variables we expect to be modified should be in this file. Some developers place the `_variables.scss` in `/Base` or `/Helpers`; Ignia, however, maintains that this file should be immediately obvious and accessible when opening the `/Styles` directory.

> *Important:* Variables defined in other files should always use the `! default` flag so they can be overwritten by `_variables.scss`.

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

## General Conventions

### Import Strategy
The projects Ignia works on come in a variety of sizes. For that reason, it is important that our SASS directory structure be comprehensive enough to accomodate large projects, without adding unnecessary complexity and overhead to small projects. To this end, we have aimed to establish a baseline structure that requires relatively few files, as well as a roadmap for how to extend that structure for (very) large projects. As a result, some concepts that are typically kept distinct in large projects (such as variables, manifests, and styles) may be conflated in smaller projects. For example, every directory (including the root) has a file in it with the same name as the ; e.g., the `/Base` directory contains a file named `_base.scss`. For a small site, this file may contain all base styles; for a larger site, however, it will likely be used exclusively as a manifest file by importing other files in the `/Base` directory. Regardless of this, authors have the assurance that all dependencies can be imported into the `/Style.scss` file by importing the `/Directory/_directory.scss' file.

> *Note:* The `/Themes` and `Views` folders may not have manifest files (e.g., `/Themes/_theme.scss`) as it is recommended that these styles be compiled independent from the centralized CSS file. For more information, see the [Themes Directory documentation](./Themes/).

### Emergent Trends
In developing our SASS structure we aimed to identify emerging trends in how other developers are structuring their SASS projects, instead of relying exclusively on our own internal conventions. This is important since Ignia works with many contractors, partners, and client developers. To this end, we leveraged commonly used folder conventions such as `/Layouts`, `/Views`, `/Helpers`, `/Components`, `/Base`, and `/Vendor`.

### Ambiguous Identifiers
Despite the above, there were a number of popular identifiers that Ignia chose not to use. These include, for instance, `/Modules`, `/Partials`, and `/Utilities`. While Ignia has our own consistent definition for each of these terms, we found that their definitions vary considerably across SASS implementations. For instance, `/Utilities` sometimes refer to CSS utility classes (e.g., `.clearfix`), other times it refers to SASS utilities, such as functions, mixins, placeholders, etc. `/Modules` was similarly confusing, as sometimes modules represent sub-components, other times the exact opposite. To avoid ambiguity when working with other developers, we consciously excluded these terms for folder names (although a `_utilities.scss` does appear under `/Base` for CSS utilities).

### Acknowledgements
In developing our SASS directory structure, Ignia relied heavily on best practices established by the broader web development community. In particular, each of the following articles played an influence in some of the conventions we have adopted.
- [Clean Out Your SASS Junk-Drawer](http://gist.io/4436524) by [Dale Sande](https://github.com/anotheruiguy)
- [Architecture for a SASS Project](http://www.sitepoint.com/architecture-sass-project/) by [Hugo Giraudel](https://github.com/HugoGiraudel)
- [How to Structure a SASS Project](http://thesassway.com/beginner/how-to-structure-a-sass-project) by [John W. Long](http://wiseheartdesign.com/)
- [Scalable and Modular Architecture for CSS](https://smacss.com/) by [Jonathan Snook](https://github.com/snookca)
