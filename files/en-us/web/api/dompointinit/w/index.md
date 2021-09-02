---
title: DOMPointInit.w
slug: Web/API/DOMPointInit/w
tags:
  - API
  - DOM
  - DOMPointInit
  - Geometry
  - Geometry Interfaces
  - Point
  - Property
  - Reference
  - W
  - perspective
browser-compat: api.DOMPointInit.w
---
{{APIRef("DOM")}}

The **{{domxref("DOMPointInit")}}** dictionary's
**`w`** property is used to specify the _w_ perspective
value of a point in space when either creating or serializing to JSON a
{{domxref("DOMPoint")}} or {{domxref("DOMPointReadOnly")}} object.

## Syntax

```js
var DOMPointInit = {
  w: wPerspective
};

DOMPointInit.w = wPerspective;

var wPerspective = DOMPointInit.w;
```

### Value

A double-precision floating-point value indicating the point's _w_ perspective
value. This value is **unrestricted**, meaning that it is allowed to be
infinite or invalid (that is, its value may be {{jsxref("NaN")}} or {{jsxref("Infinity",
  "±Infinity")}}).

There are two methods which use `DOMPointInit`:

- The static function {{domxref("DOMPointReadOnly.fromPoint()")}} takes an object that
  complies with `DOMPointInit` as its sole input parameter, to specify the
  coordinates and perspective value of the new point to be created. This method is, by
  inheritance, also available as {{domxref("DOMPoint.fromPoint()")}}.
- The {{domxref("DOMPointReadOnly.toJSON()")}} method returns a
  `DOMPointInit` object that describes the same point as the original point.
  By inheritance, this method is also available as {{domxref("DOMPointReadOnly.toJSON")}}.

This value is assumed to be 1 by default if not included in the
`DOMPointInit` object passed into `fromPoint()`.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
