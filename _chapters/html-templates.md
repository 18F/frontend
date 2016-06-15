---
title: HTML Templates
---
The `<template>` element is officially part of the [HTML5 living
standard][HTML template], and [you can use it][caniuse/template] in _most_
modern browsers (with the exception of IE; it is supported by Edge 13 and
above) without a [polyfill](#web-component-polyfills). It works like this:

* `<template>` elements are never displayed by the browser, but are part of
  the document and can be targeted with `document.querySelector()` or
  `document.getElementById()`.
* In JavaScript, a `<template>` element's `content` property is a [document
  fragment][DocumentFragment] that can be [cloned][Node.cloneNode], modified,
  and appended elsewhere in the document.

For example:

```html
<template id="my-template">
  <li class="item"><a href="#"></a></li>
</template>
<ul id="items"></ul>
<script>
var template = document.querySelector('#my-template').content;
var list = document.querySelector('#items');
['foo', 'bar', 'baz'].forEach(function(x) {
  var item = template.cloneNode(true);
  var a = item.querySelector('a');
  a.href = '#' + x;
  a.textContent = x;
  list.appendChild(item);
});
</script>
```

> HTML templates are a great choice for marking up data templates because
> they're invisible by default and, unlike `<script>` elements with exotic
> `type` attributes, they have a native DOM that can be cloned, modified, and
> inserted more efficiently than getting and setting `innerHTML`.

* [HTML5 Rocks HTML Template tutorial](http://www.html5rocks.com/en/tutorials/webcomponents/template/)

[DocumentFragment]: https://developer.mozilla.org/en-US/docs/Web/API/DocumentFragment
[HTML template]: https://www.w3.org/TR/html5/scripting-1.html#the-template-element
[Node.cloneNode]: https://developer.mozilla.org/en-US/docs/Web/API/Node/cloneNode
[caniuse/template]: http://caniuse.com/#feat=template
