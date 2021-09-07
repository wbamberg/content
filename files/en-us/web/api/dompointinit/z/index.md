---
title: DOMPointInit.z
slug: Web/API/DOMPointInit/z
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
  - z
browser-compat: api.DOMPointInit.z
---
{{APIRef("DOM")}}

The **{{domxref("DOMPointInit")}}** dictionary's
**`z`** property is used to specify the _z_-coordinate
of a point in 2D or 3D space when either creating or serializing to JSON a
{{domxref("DOMPoint")}} or {{domxref("DOMPointReadOnly")}} object.

Typically, a `z` value of 0 represents the plane of the screen. As the value
increases, the point moves outward from the screen toward the user. As the value
decreases, the point moves farther from the user, with negative values being behind the
screen, receding into the distance.

Of course, if [transforms](/en-US/docs/Web/CSS/CSS_Transforms) have been
applied, the axes may have changed orientation.

## Syntax

```js
var DOMPointInit = {
  z: zPos
};

DOMPointInit.z = zPos;

var zPos = DOMPointInit.z;
```

### Value

A double-precision floating-point value indicating the point's _z_-coordinate.
This value is **unrestricted**, meaning that it is allowed to be infinite
or invalid (that is, its value may be {{jsxref("NaN")}} or {{jsxref("Infinity",
  "±Infinity")}}).

There are two methods which use `DOMPointInit`:

- The static function {{domxref("DOMPointReadOnly.fromPoint()")}} takes an object that
  complies with `DOMPointInit` as its sole input parameter, to specify the
  coordinates and perspective value of the new point to be created. This method is, by
  inheritance, also available as {{domxref("DOMPoint.fromPoint()")}}.
- The {{domxref("DOMPointReadOnly.toJSON()")}} method returns a
  `DOMPointInit` object that describes the same point as the original point.
  By inheritance, this method is also available as {{domxref("DOMPointReadOnly.toJSON")}}.

If this property is missing when the `DOMPointInit` object is passed into
`fromPoint()`, the value is assumed to be 0 by default.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
