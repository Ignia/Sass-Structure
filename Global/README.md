# Global Directory

Ignia has a number of global SASS files that we use for all (or, at least, most) of our projects. This includes some default styles, styles specific to administrative tools, and reusable mixins and functions. In each case, these are located in a subdirectory `/Global`; e.g., `/Global/Admin/`. These should be imported into the main `_global.scss` file as required by the project. As with third-party vendor files, files within /Global should not be updated (outside of the `_global.scss` manifest), as these will be maintained independently by Ignia.

