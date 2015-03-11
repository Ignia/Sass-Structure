# Helpers Directory

Helpers provide, exclusively, functional code that don’t output style declarations directly. For many sites, it may be enough to simply place these in the `/Helpers` folder. By default, these can be placed in the '_helpers.scss` file; for more complex structures, however, helpers should be broken down by type; this may include, for instance, placeholders (in `_placeholders.scss`), mix-ins (in `_mixins.scss`), and functions (in `_functions.scss`). For a *very* large site, it may be preferable to break up these files into even smaller components; in this case, it is recommended that partials be created in associated subfolders (e.g., `/Helpers/Mixins/`), and the associated manifest (e.g., `_mixins.scss`) moved into that subdirectory.



