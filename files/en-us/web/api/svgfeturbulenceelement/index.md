---
title: SVGFETurbulenceElement
slug: Web/API/SVGFETurbulenceElement
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGFETurbulenceElement
---
{{APIRef("SVG")}}

The **`SVGFETurbulenceElement`** interface corresponds to the {{SVGElement("feTurbulence")}} element.

{{InheritanceDiagram(600, 140)}}

## Constants

### Turbulence types

| Name                               | Value | Description                                                                                                                                                  |
| ---------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `SVG_TURBULENCE_TYPE_UNKNOWN`      | 0     | The type is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| `SVG_TURBULENCE_TYPE_FRACTALNOISE` | 1     | Corresponds to the `fractalNoise` value.                                                                                                                     |
| `SVG_TURBULENCE_TYPE_TURBULENCE`   | 2     | Corresponds to `turbulence` value.                                                                                                                           |

### Stitch options

| Name                      | Value | Description                                                                                                                                                  |
| ------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `SVG_STITCHTYPE_UNKNOWN`  | 0     | The type is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| `SVG_STITCHTYPE_STITCH`   | 1     | Corresponds to the `stitch` value.                                                                                                                           |
| `SVG_STITCHTYPE_NOSTITCH` | 2     | Corresponds to `noStitch` value.                                                                                                                             |

## Properties

_This interface also inherits properties from its parent interface, {{domxref("SVGElement")}}._

- {{domxref("SVGFETurbulenceElement.baseFrequencyX")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedNumber")}} corresponding to the X component of the {{SVGAttr("baseFrequency")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.baseFrequencyY")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedNumber")}} corresponding to the Y component of the {{SVGAttr("baseFrequency")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.height")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedLength")}} corresponding to the {{SVGAttr("height")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.numOctaves")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedInteger")}} corresponding to the {{SVGAttr("numOctaves")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.result")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedString")}} corresponding to the {{SVGAttr("result")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.seed")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedNumber")}} corresponding to the {{SVGAttr("seed")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.stitchTiles")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedEnumeration")}} corresponding to the {{SVGAttr("stitchTiles")}} attribute of the given element. It takes one of the `SVG_STITCHTYPE_*` constants defined on this interface.
- {{domxref("SVGFETurbulenceElement.type")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedEnumeration")}} corresponding to the {{SVGAttr("type")}} attribute of the given element. It takes one of the `SVG_TURBULENCE_TYPE_*` constants defined on this interface.
- {{domxref("SVGFETurbulenceElement.width")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedLength")}} corresponding to the {{SVGAttr("width")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.x")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedLength")}} corresponding to the {{SVGAttr("x")}} attribute of the given element.
- {{domxref("SVGFETurbulenceElement.y")}} {{ReadOnlyInline}}
  - : An {{domxref("SVGAnimatedLength")}} corresponding to the {{SVGAttr("y")}} attribute of the given element.

## Methods

_This interface does not provide any specific methods, but implements those of its parent, {{domxref("SVGElement")}}._

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{SVGElement("feTurbulence")}}
