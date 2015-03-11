# Vendor Directory

Code provided by third parties should be placed in the `/Vendor` directory. This may include code tied to particular components (e.g., a jQuery library), or a UI Framework (such as Bootstrap, Foundation, or Semantic-UI).

Code under these directories should *no*t be modified; if needed, overrides should be placed in the `/Overrides` directory instead.

The one exception is configuration files, such as Bootstrap’s `_variables.scss` file. That said, if you’re using a large UI Framework like bootstrap, Ignia’s SASS directory structure is probably overkill for your needs.

 Vendor files should be imported via the `_vendor.scss` file, which provides a manifest of vendor dependencies.
