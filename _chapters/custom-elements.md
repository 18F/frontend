---
title: Custom Elements
---

## `document.registerElement()`
[Andrea Giammarchi's](http://webreflection.blogspot.com/2014/07/a-w3c-custom-elements-alternative.html)
[document-register-element] polyfill for the ["v1" custom elements
API][custom elements v1] is lightweight and solid, but provides only the
low-level `document.registerElement()` API.

1. At just 3K minified and zipped, it's *tiny* compared to Polymer's hefty
   150K payload (after you include all of the necessary polyfills).
2. It works in IE9 if you include either [aight] or Andrea's [dom4] polyfill.
3. The API does exactly what the [spec][custom elements v1] says it should,
   and nothing more. No two-way data binding, no event delegation, no
   performance-hobbling shadow DOM shims (or shams).

> Verdict: **Use this! It works great!**

[aight]: https://github.com/shawnbot/aight
[custom elements v1]: https://www.w3.org/TR/2016/WD-custom-elements-20160226/
[document-register-element]: https://github.com/WebReflection/document-register-element
[dom4]: https://github.com/WebReflection/dom4
