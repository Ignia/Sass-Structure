# Global Directory

For organizations with multiple projects or products, such as Ignia, it is likely that a set of Sass files will be established across the organization. This may include, for instance, a standard library of helpers or baseline themes to be shared across multiple sites. These shared components go in the `/Global` directory, and are imported into the  `_global.scss` file as required.

## Files
The directory structure of `/Global` should mimic that of the root Sass structure. So, for instance, Ignia has a global theme for all administrative sites; we place that in `/Global/Themes/Admin/`. 

> *Note:* As with third-party vendor files, files within `/Global` should not be updated (outside of the `_global.scss` manifest), as these will be maintained independent of any single project. In a centralized development process, this may be maintained by using symbolic links. 

