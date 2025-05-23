---
title: "ElementInternals: ariaMultiLine property"
short-title: ariaMultiLine
slug: Web/API/ElementInternals/ariaMultiLine
page-type: web-api-instance-property
browser-compat: api.ElementInternals.ariaMultiLine
---

{{APIRef("Web Components")}}

The **`ariaMultiLine`** property of the {{domxref("ElementInternals")}} interface reflects the value of the [`aria-multiline`](/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-multiline) attribute, which indicates whether a text box accepts multiple lines of input or only a single line.

> [!NOTE]
> Setting aria attributes on `ElementInternals` allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the [Accessibility Object Model explainer](https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object).

## Value

A string with one of the following values:

- `"true"`
  - : This is a multi-line text box.
- `"false"`
  - : This is a single-line text box.

## Examples

In this example the value of `ariaMultiLine` is set to "true".

```js
class CustomControl extends HTMLElement {
  constructor() {
    super();
    this.internals_ = this.attachInternals();
    this.internals_.ariaMultiLine = "true";
  }
  // …
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [ARIA: textbox role](/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/textbox_role)
