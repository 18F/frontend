---
title: Frameworks
permalink: /css/frameworks/
sidenav: css
---
# Frameworks

18F currently recommends using the [U.S. Web Design System](https://github.com/uswds/uswds) as it is specifically designed to help build fast, accessible, mobile-friendly federal government websites.

Sometimes, projects utilize other CSS frameworks such as:

- [Bourbon](https://www.bourbon.io/) (particularly well-suited to working with Sass)
- [BassCSS](https://www.basscss.com/) (atomic CSS framework)

These frameworks were chosen because they're relatively unopinionated about
design decisions while still providing the helpers that make frameworks
essential to fast and accurate front-end work (for example, solutions for
responsive design, grids, and common design patterns). In addition, both
frameworks, through modular design and excellent documentation, make it easy
for the designer or developer to only use the parts that they need, rather than
including a hefty library.

## Considerations for choosing a CSS framework

When choosing a framework for your project, the following questions may be helpful in assessing your options:

- What does it offer that the U.S. Web Design System doesn't?
- How does it support responsive design?
- Are patterns for more complex interactions (accordions, tabs, menus) accessible?
- Does it allow for straightforward customization?
- Is it mature and currently supported?
- Does it support older browsers and provide fallbacks for newer techniques when necessary?
- Is the library size reasonable?
- Do other developers and designers on your team know how to work with this framework?

## Do not use Bootstrap
18F specifically does not recommend using [Bootstrap](http://getbootstrap.com/) for production work
because it can be difficult to adapt its opinionated styles to bespoke design work.
