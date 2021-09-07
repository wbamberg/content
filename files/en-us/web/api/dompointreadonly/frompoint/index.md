---
title: DOMPointReadOnly.fromPoint()
slug: Web/API/DOMPointReadOnly/fromPoint
tags:
  - API
  - Coordinates
  - DOM
  - DOMPointReadOnly
  - Geometry
  - Geometry Interfaces
  - Method
  - Point
  - Reference
  - Static Method
  - fromPoint
browser-compat: api.DOMPointReadOnly.fromPoint
---
{{APIRef("DOM")}}

The static **{{domxref("DOMPointReadOnly")}}**
method `fromPoint()` creates and returns a new
`DOMPointReadOnly` object given a source point.

The source point is
specified as a {{domxref("DOMPointInit")}}-compatible object, which includes both
{{domxref("DOMPoint")}} and {{domxref("DOMPointReadOnly")}}.

You can also create a new `DOMPointReadOnly` object using the
{{domxref("DOMPointReadOnly.DOMPointReadOnly", "new DOMPointReadOnly()")}} constructor.

## Syntax

```js
const point = DOMPointReadOnly.fromPoint(sourcePoint)
```

### Properties

- `sourcePoint`
  - : A {{domxref("DOMPointInit")}}-compliant object, which includes both
    {{domxref("DOMPoint")}} and {{domxref("DOMPointReadOnly")}}, from which to take the
    values of the new point's properties.

### Return value

A new {{domxref("DOMPointReadOnly")}} object (which is identical to the source point).

## Examples

### Creating a 2D point

This sample creates a 2D point, specifying an inline object that includes the values to
use for {{domxref("DOMPointReadOnly.x", "x")}} and {{domxref("DOMPointReadOnly.y",
  "y")}}. The `z` and `w` properties are allowed to keep their
default values (`0` and `1` respectively).

```js
const point2D = DOMPointReadOnly.fromPoint({x: 25, y: 25})
```

### Creating a 3D point using an existing point

This example creates a point, `origPoint`, of type
{{domxref("DOMPoint")}}, using {{domxref("DOMPoint.DOMPoint", "new DOMPoint()")}}. That
point is then used as the input for `fromPoint()` to create a new point,
`newPoint`.

```js
const origPoint = new DOMPoint(25, 25, 100, 0.5)

const newPoint = DOMPointReadOnly.fromPoint(origPoint)
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
