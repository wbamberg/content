---
title: DOMPoint.fromPoint()
slug: Web/API/DOMPoint/fromPoint
tags:
  - API
  - Coordinates
  - DOM
  - DOMPoint
  - Geometry
  - Geometry Interfaces
  - Method
  - Point
  - Reference
  - Static
  - Static Method
  - fromPoint
browser-compat: api.DOMPoint.fromPoint
---
{{APIRef("DOM")}}

The static **{{domxref("DOMPoint")}}** method
`fromPoint()` creates and returns a new mutable `DOMPoint`
object given a source point.

The source point is specified as a
{{domxref("DOMPointInit")}}-compatible object, which includes both
{{domxref("DOMPoint")}} and {{domxref("DOMPointReadOnly")}}.

You can also create a new `DOMPoint` object using the
{{domxref("DOMPoint.DOMPoint", "new DOMPoint()")}} constructor.

Although this interface is based on `DOMPointReadOnly`, it is not read-only;
the properties within may be changed at will.

## Syntax

```js
var point = DOMPoint.fromPoint(sourcePoint);
```

### Properties

- `sourcePoint`
  - : A {{domxref("DOMPointInit")}}-compliant object, which includes both
    {{domxref("DOMPoint")}} and {{domxref("DOMPointReadOnly")}}, from which to take the
    values of the new point's properties.

### Return value

A new {{domxref("DOMPoint")}} object whose coordinate and perspective values are
identical to those in the source point. The point's properties are mutable and may be
changed at any time.

## Examples

### Creating a mutable point from a read-only point

If you have a {{domxref("DOMPointReadOnly")}} object, you can easily create a mutable
copy of that point:

```js
var mutablePoint = DOMPoint.fromPoint(readOnlyPoint);
```

### Creating a 2D point

This sample creates a 2D point, specifying an inline object that includes the values to
use for {{domxref("DOMPointReadOnly.x", "x")}} and {{domxref("DOMPointReadOnly.y",
  "y")}}. The _z_ and _w_ properties are allowed to keep their default
values (0 and 1 respectively).

```js
var center = DOMPoint.fromPoint({x: 75, y: -50, z: -55, w: 0.25});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
