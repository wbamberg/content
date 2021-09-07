---
title: DOMPointInit.y
slug: Web/API/DOMPointInit/y
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
  - 'y'
browser-compat: api.DOMPointInit.y
---
{{APIRef("DOM")}}

The **{{domxref("DOMPointInit")}}** dictionary's
**`y`** property is used to specify the _y_-coordinate
of a point in 2D or 3D space when either creating or serializing to JSON a
{{domxref("DOMPoint")}} or {{domxref("DOMPointReadOnly")}} object.

In general, the value of `y` increases to the right and decreases to the
left, becoming negative to the left of the origin. This may change if transforms have
been applied causing the axes' orientation to change.

## Syntax

```js
var DOMPointInit = {
  y: yPos
};

DOMPointInit.y = yPos;

var yPos = DOMPointInit.y;
```

### Value

A double-precision floating-point value indicating the point's _y_-coordinate.
This value is **unrestricted**, meaning that it is allowed to be infinite
or invalid (that is, its value may be {{jsxref("NaN")}} or {{jsxref("Infinity",
  "±Infinity")}}).

If this property is missing when the `DOMPointInit` object is passed into
`fromPoint()`, the value is assumed to be 0 by default.

There are two methods which use `DOMPointInit`:

- The static function {{domxref("DOMPointReadOnly.fromPoint()")}} takes an object that
  complies with `DOMPointInit` as its sole input parameter, to specify the
  coordinates and perspective value of the new point to be created. This method is, by
  inheritance, also available as {{domxref("DOMPoint.fromPoint()")}}.
- The {{domxref("DOMPointReadOnly.toJSON()")}} method returns a
  `DOMPointInit` object that describes the same point as the original point.
  By inheritance, this method is also available as {{domxref("DOMPointReadOnly.toJSON")}}.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
