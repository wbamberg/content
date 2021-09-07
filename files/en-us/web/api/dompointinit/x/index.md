---
title: DOMPointInit.x
slug: Web/API/DOMPointInit/x
tags:
  - API
  - Coordinates
  - DOM
  - DOMPointInit
  - Geometry
  - Geometry Interfaces
  - Point
  - Property
  - Reference
  - x
browser-compat: api.DOMPointInit.x
---
{{APIRef("DOM")}}

The **{{domxref("DOMPointInit")}}** dictionary's
**`x`** property is used to specify the x component of a point
in 2D or 3D space when either creating or serializing a {{domxref("DOMPoint")}} or
{{domxref("DOMPointReadOnly")}}.

In general, positive values `x` mean to the right, and negative values of
`x` means to the left, assuming that transforms have not altered the
orientation of the axes.

## Syntax

```js
var DOMPointInit = {
  x: xPos
};

DOMPointInit.x = xPos;

var xPos = DOMPointInit.x;
```

### Value

A double-precision floating-point value indicating the point's x coordinate. This value
is **unrestricted**, meaning that it is allowed to be infinite or invalid
(that is, its value may be {{jsxref("NaN")}} or {{jsxref("Infinity", "±Infinity")}}).

If this property is missing when the `DOMPointInit` object is passed into
`fromPoint()`, the value is assumed to be 0 by default.

`DOMPointInit` is used as an input when calling either
{{domxref("DOMPointReadOnly.fromPoint()")}} or {{domxref("DOMPoint.fromPoint()")}}, and
is returned by the {{domxref("DOMPointReadOnly.toJSON()")}} and
{{domxref("DOMPointReadOnly.toJSON")}} methods.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
