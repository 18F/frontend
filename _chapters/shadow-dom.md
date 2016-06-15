---
title: Shadow DOM
---
The so-called "shadow DOM" is an encapsulation of the [Document Object
Model][DOM] designed specifically to prevent the elements and styles of web
components from being affected by (and "leaking" into) their parent document.

> **Shadow DOM an experimental technology,** but the [draft spec], which
> [Chrome](https://www.chromestatus.com/features/4667415417847808) refers to
> as the "v1 API", has been agreed upon by all of the major browser vendors.
> The [webcomponents.js] suite includes a polyfill for the v1 APIs, but
> because _true_ encapsulation requires shimming low-level DOM APIs, **this
> polyfill may inflict significant performance penalties**.

[draft spec]: https://www.w3.org/TR/shadow-dom/
[webcomponents.js]: https://github.com/WebComponents/webcomponentsjs
