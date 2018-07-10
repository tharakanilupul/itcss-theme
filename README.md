# Codegen - Sass Architecture Structure [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of awesome [ITCSS](http://itcss.io/) articles, and resources.

```
sass/
|
|– theme-settings/
|   |– _color.scss       # Theme colors
|   |– _brand.scss       # Brand logo
|   |– _font.scss        # Theme fonts
|   |– _icon.scss        # Icons
|   ...                  # Etc…
|
|– tools/
|   |– functions/        # Sass Functions
|   |– mixins/           # Sass Mixins
|   ...                  # Etc…
|
|– generic/
|   |– _normalize.scss   # Normalize
|   |– _reset.scss       # Reset
|   |– _base.scss        # Base rules
|
|– objects/
|   |– atoms/            # Atoms
|   |– molecules/        # Molecules
|   |– organism/         # Organism
|
|– layouts/
|   |– _grid.scss        # Grid
|   ...                  # Etc…
|
|– components/
|   |– _sample.scss      # Grid
|   ...                  # Etc…
|
|– pages/
|   |– _details.scss     # Grid
|   ...                  # Etc…
|
|– layout/
|   |– _navigation.scss  # Navigation
|   |– _grid.scss        # Grid system
|   |– _header.scss      # Header
|   |– _footer.scss      # Footer
|   |– _sidebar.scss     # Sidebar
|   |– _forms.scss       # Forms
|   ...                  # Etc…
|
|– pages/
|   |– _home.scss        # Home specific styles
|   |– _contact.scss     # Contact specific styles
|   ...                  # Etc…
|
|– utilities/
|   |– _clearfix.scss    # Clearfix
|   |– _helpers.scss     # Class & placeholders helpers
|
|
`– styles.scss            # Primary Sass file
```

### THEME SETTINGS FOLDER

Variables and other settings. Used with preprocessors and contain font, colors definitions, etc.

### TOOLS FOLDER

The `tools/` folder gathers all Sass tools and helpers used across the project. Every function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. These are nothing but Sass helpers.

### GENERIC FOLDER

Reset and/or normalize styles and also styling for bare HTML elements (like h1, a etc.). This is the first layer which generates actual CSS.

### OBJECTS FOLDER

`Atoms`, `Molecules` and `Organism` level style files include in `objects\` folder. These styles are common accross all over the project.

### LAYOUT FOLDER

Globally defined class-based selectors that used for layouting purposes.

### COMPONENTS FOLDER

Specific UI components. This is where majority of our work takes place and our UI components are often composed of Objects and Components

### PAGES FOLDER

If you have page-specific styles, it is better to put them in a `pages/` folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a `_home.scss` file in `pages/`.

### UTILITIES FOLDER

This will generate some helper classes. The `uitities/` folder gathers all Sass helpers used across the project.

### STYLES.SCSS FILE

The style file should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@import` and comments.

Files should be imported according to the folder they live in, one after the other in the following order:

1. `theme-settings/`
2. `tools/`
3. `generic/`
4. `objects/`
5. `layout/`
6. `components/`
7. `pages/`
8. `utilities/`

## Diagram 

> [![Awesome](https://i.imgur.com/NTYt2ab.png)](https://github.com/sindresorhus/awesome)]

## Articles

- [Manage large-scale web projects with new CSS architecture ITCSS](http://www.creativebloq.com/web-design/manage-large-scale-web-projects-new-css-architecture-itcss-41514731)
- [ITCSS: SCALABLE AND MAINTAINABLE CSS ARCHITECTURE](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)
- [Building a Maintainable and Scalable CSS Codebase with ITCSS](https://medium.okgrow.com/building-a-maintainable-and-scalable-css-codebase-with-itcss-ceda5b2f495b#.m6l7sx48c)
- [The BEMIT naming convention](http://www.jamesturneronline.net/blog/bemit-naming-convention.html)
- [CSS at trivago — Part 1: Structure and ITCSS](https://medium.com/@pistenprinz/css-at-trivago-part-1-structure-and-itcss-52f63ed557ca#.abr0loev4)
- [CSS at trivago — Part 2: Naming Conventions and Methodologies](https://medium.com/@pistenprinz/css-at-trivago-part-2-naming-conventions-and-methodologies-d51b445a3a39)

## Videos

- [Manage large CSS projects with ITCSS Screencast](https://www.youtube.com/watch?v=hz76JIU_xB0)
- [Harry Roberts - Managing CSS Projects with ITCSS](https://www.youtube.com/watch?v=1OKZOV-iLj4) - [SLides](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)

## Code Examples

- [itcss-netmag](https://github.com/itcss/itcss-netmag)
- [frcss](https://github.com/csswizardry/frcss)
- [inuitcss](https://github.com/inuitcss/inuitcss)
- [CSS Wizardry](https://github.com/csswizardry/csswizardry.github.com/tree/master/css)
- [GOV.UK Frontend Alpha](https://github.com/alphagov/govuk_frontend_alpha/tree/master/app/assets/scss)
- [iotaCSS](https://www.iotacss.com/)
- [BBC Grandstand](https://github.com/bbc/grandstand)

## License

Copyright (c) 2018. CodeGen Ltd. - All Rights Reserved





