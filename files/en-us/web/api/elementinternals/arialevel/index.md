---
title: "ElementInternals: ariaLevel property"
short-title: ariaLevel
slug: Web/API/ElementInternals/ariaLevel
page-type: web-api-instance-property
browser-compat: api.ElementInternals.ariaLevel
---

{{APIRef("Web Components")}}

The **`ariaLevel`** property of the {{domxref("ElementInternals")}} interface reflects the value of the [`aria-level`](/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-level) attribute, which defines the hierarchical level of an element within a structure.

> [!NOTE]
> Setting aria attributes on `ElementInternals` allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the [Accessibility Object Model explainer](https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object).

## Value

A string containing an integer.

## Examples

In this example the value of `ariaLevel` is set to "1".

```js
class CustomEl extends HTMLElement {
  constructor() {
    super();
    this.internals_ = this.attachInternals();
    this.internals_.ariaLevel = "1";
  }
  // …
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [ARIA: heading role](/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/heading_role)
