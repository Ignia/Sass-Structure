# Vendor Directory

Code provided by third parties should be placed in the `/Vendor` directory. This may include code tied to particular components (e.g., a jQuery library), or a UI Framework (such as Bootstrap, Foundation, or Semantic-UI).

> **Important:** Code under these directories should *not* be modified; if needed, overrides should be placed in the `/Overrides` directory instead.

## Files
Vendor files should each be placed in their own file. Typically, the file names will be defined by the vendor; these should not be changed unless they are ambiguous (rare). Each vendor file should be imported into the `_vendor.scss` file, which provides a manifest of vendor dependencies.

> *Note:* No styles should live in the `_vendor.scss`; this should *only* include `@import` statements. 
