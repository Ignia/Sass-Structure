# Ignia SASS Structure
Ignia's internal file and directory structure for CSS pre-compiled using SASS.

## Directories
- [ ] [Base](./Base/)
- [ ] [Components](./Components/)
  - [ ] [ComponentA](./Components/ComponentA/)
- [ ] [Global](./Global/)
  - [ ] [Defaults](./Global/Defaults/)
  - [ ] [Admin](./Global/Admin/)
  - [ ] [Helpers](./Global/Helpers/)
- [ ] [Helpers](./Helpers/)
- [ ] [Layout](./Layout/)
- [ ] [Overrides](./Overrides/)
- [ ] [Themes](./Themes/)
  - [ ] [Brand](./Themes/Brand/)
  - [ ] [Theme](./Themes/Theme/)
- [ ] [Vendor](./Vendor/)
- [ ] [Views](./Views/)


## Variables
Ignia put the `_variables.scss` file in the root as, ideally, that is the first stop for maintaining the site styles after the site has been built. For more invasive updates or refreshes, developers will certainly need to dive into other directories, but any variables we expect to be modified will be in this file. Others sometimes place this file in `/Base` or `/Helpers`; we feel it is important that this file be immediately obvious. Variables defined in other files should always use the `! default` flag so they can be overwritten by `_variables.scss`.

## General Conventions

### Import Strategy
This section is a placeholder, and still needs to be completed.

### Emergent Trends
In developing our SASS structure we aimed to identify emerging trends in how other developers are structuring their SASS projects, instead of relying exclusively on our own internal conventions. This is important since Ignia works with many contractors, partners, and client developers. To this end, we leveraged commonly used folder conventions such as `/Layouts`, `/Views`, `/Helpers`, `/Components`, `/Base`, and `/Vendor`.

### Ambiguous Identifiers
Despite the above, there were a number of popular identifiers that Ignia chose not to use. These include, for instance, `/Modules`, `/Partials`, and `/Utilities`. While Ignia has our own consistent definition for each of these terms, we found that their definitions vary considerably across SASS implementations. For instance, `/Utilities` sometimes refer to CSS utility classes (e.g., `.clearfix`), other times it refers to SASS utilities, such as functions, mixins, placeholders, etc. `/Modules` was similarly confusing, as sometimes modules represent sub-components, other times the exact opposite. To avoid ambiguity when working with other developers, we consciously excluded these terms for folder names (although a `_utilities.scss` does appear under `/Base` for CSS utilities).
