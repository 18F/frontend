---
title: HTML Imports
---
HTML imports are a [W3C working draft][HTML imports] that allows web
components to be "packaged" as HTML files that can be imported into other
documents with a `<link>` tag:

```html
<link rel="import" href="path/to/my-component.html">
```

Each HTML import implements a unique [custom element](#custom-elements), and
can reference its own CSS and JavaScript, either inline or via external
references. Imports often leverage [HTML templates](#html-templates), and can
achieve full style encapsulation with the [shadow DOM](#shadow-dom).

> **HTML imports are an experimental technology.** As of June, 2016,
> [Chrome](https://www.chromestatus.com/features/5144752345317376) is the only
> browser that offers a native implementation. Though Firefox support is
> [apparently in the works](https://bugzilla.mozilla.org/show_bug.cgi?id=877072),
> Microsoft is still only [considering](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/htmlimports?filter=f3f0000bf&search=import)
> support in Edge, and WebKit (Safari) has yet to pledge support for the
> [draft spec][HTML imports]. The [webcomponents.js] polyfill
> [works](https://github.com/WebComponents/webcomponentsjs#browser-support)
> in all modern browsers.

[HTML imports]: https://www.w3.org/TR/html-imports/
[webcomponents.js]: https://github.com/WebComponents/webcomponentsjs
