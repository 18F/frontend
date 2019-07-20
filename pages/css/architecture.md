---
title: Architecture
permalink: /css/architecture/
sidenav: css
---
# Choosing a CSS methodology and architecture
A site's architecture should be based on its goals and purposes. This means the
guidance here should be adapted to different sites and situations.

In general, 18F recommends using a modular approach (specifically, [modified BEM])
to provide consistency and scalability to larger apps. However, for some applications
(such as a rapid prototype), an atomic architecture may make more sense. Below are 
some considerations for choosing an architecture.

## Modular architecture
Naming conventions like [BEM] and [SMACSS] popularized the idea of modular architecture.
Modular architectures are very helpful for a few different kinds of projects:
- larger, more complex sites with reusable components
- sites maintained and built by multiple engineers
- production sites that will be handed off to partner teams or vendors

In a modular architecture, every page is broken into `components` and `modules`.
*Components* provide basic recurring elements such as buttons, lists, and navs. 
*Modules* are built by combining these components into reusable structures.
This helps keep the specificity trend in an upwards curve as you move down in the file
(more on this to come).

A few helpful things to keep in mind when building out a modular architecture:
- Start with an elements file for all tag rules (`a`, `h1`-`h5`, `p`, `*`, `html`, `body`).
- Create component files for each structural element, such as buttons, navs,
  etc.
- Create more specific structure with modules. For instance, if the logo image
  and text needs very specific treatment, use a module.
  - Build modules from components through Sass mixins, extends, and HTML.
- Have an overrides file or folder comprised of global rules that are meant to
  override components and modules.
  - These can be generic utilities.
  - A good thing to put here are breakpoint-specific rules, such as hiding
    something at small breakpoints.

### Example file structure
```sh
_elements.scss
_mixins.scss
_typography.scss
_util.scss
_vars.scss
component/_blurb.scss
component/_button.scss
component/_island.scss
component/_sub_nav.scss
module/_logo.scss
module/_progress_bar.scss
lib/bourbon.scss
lib/neat.scss
_overrides.scss
```

## Atomic architecture



[BEM]: http://getbem.com/introduction/
[SMACSS]: http://smacss.com/
[modified BEM]: /css/naming