---
title: SVGZoomAndPan
slug: Web/API/SVGZoomAndPan
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGZoomAndPan
---
{{deprecated_header}}

The **`SVGZoomAndPan`** interface is used to reflect the {{SVGAttr("zoomAndPan")}} attribute, and is mixed in to other interfaces for elements that support this attribute.

{{InheritanceDiagram}}

## Constants

| Name                     | Value | Description                                                                                                                                                  |
| ------------------------ | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `SVG_ZOOMANDPAN_UNKNOWN` | 0     | The type is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| `SVG_ZOOMANDPAN_DISABLE` | 1     | Corresponds to the value `disable`.                                                                                                                          |
| `SVG_ZOOMANDPAN_MAGNIFY` | 2     | Corresponds to the value `magnify`.                                                                                                                          |

## Properties

- {{domxref("SVGZoomAndPan.zoomAndPan")}}
  - : An unsigned short representing the value of the {{SVGAttr("zoomAndPan")}} attribute.

## Methods

_This interface doesn't implement any specific methods._

## Browser compatibility

{{Compat}}

## See also

- {{SVGAttr("zoomAndPan")}}
