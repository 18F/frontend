---
title: Documentation
permalink: /css/documentation/
sidenav: css
---
# Documentation

You should always document:
- Magic numbers (when you absolutely cannot avoid using them)
- Overrides of imported frameworks like USWDS
- Rules that must be used in conjunction with one another
(using BEM naming conventions is somewhat self-documenting in this regard)

We also recommend maintaining a project style guide of your choice.
Add examples of how to use classes that make up complex modules
when used in conjunction with one another.

## Sass Comments
Be intentional when you use `//` (silent comments) versus `/* */`
(which are preserved in the CSS output). When in doubt, use `//`.

## KSS
KSS is the most common CSS documentation method to date. It relies
on comments that follow a specific format to generate documentation
for you. The generated documentation can be modified through templates.
More information on KSS can be found on the
[official KSS site](http://warpspire.com/kss/).

The original KSS repo is not maintained. There are numerous forks that are
maintained, the [Node.js KSS fork](https://github.com/kss-node/kss-node) being
one of the more active ones.

### Example of KSS documentation

```scss
// Button
//
// Various buttons on the site.
//
// Markup
// <a class="button {{ modifier_class }}">
//  <span class="button__text">Link</span
// </a>
//
// .button-modified - A button with a different style.
//
//
// Styleguide component.button
.button {
}

.button-modified {
}
```
