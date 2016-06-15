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
1. Chrome added native support for `document.registerElement()` in [version
   33](https://www.chromestatus.com/features/4642138092470272) (released
   February, 2014). This means that you can test the technology more with a
   stable, native implementation first, then compare the results of your test
   with polyfilled browsers.

> **Use this! It works great!** And though the ["v1" API has already
> been deprecated][custom elements v2], this polyfill is simple enough that it
> _should_ contiunue working even after Chrome sunsets
> `document.registerElement()`.

[aight]: https://github.com/shawnbot/aight
[custom elements v1]: https://www.w3.org/TR/2016/WD-custom-elements-20160226/
[custom elements v2]: https://www.w3.org/TR/custom-elements/
[document-register-element]: https://github.com/WebReflection/document-register-element
[dom4]: https://github.com/WebReflection/dom4
