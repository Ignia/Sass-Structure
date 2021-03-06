# Overrides Directory

When relying on third-party or centralized styles (such as a Sass-based UI framework, or a company-wide `/Themes/Brand/` style), it is likely that some styles will need to be overwritten. Ideally, this will be done by modifying variables or supplying optional placeholders. When these options are not viable, however, the `/Overrides` directory provides a centralized place to deal with these.

## Scaling
By default, overrides should go into the `_overrides.scss` file, but if there are many overrides specific to a particular library, they may be placed in an `/Overrides/_vendor.scss` file or, perhaps, an `/Overrides/_brand.scss` file. In either case, the file should be imported at the top of the `_overrides.scss` file.

## Hacks
The `_hacks.scss` file is based on [CSS Wizardry](http://csswizardry.com/)’s [shame.css proposal](http://csswizardry.com/2013/04/shame-css/), which is a location to put “bad” code. Ideally, this file will always be empty, but in real world applications, hacks are often required for backward compatibility, browser idiosyncrasies, or complexities in playing nicely with third-party code. By centralizing these in a single file, a site maintains a “todo” list of styles that should be reevaluated in the future to determine if they’re still necessary. In Ignia’s experience, hacks are almost always associated with overrides and working with third-party frameworks, and so we’ve placed this inside of our `/Overrides` folder.


