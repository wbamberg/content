---
title: SVGRenderingIntent
slug: Web/API/SVGRenderingIntent
tags:
  - API
  - Deprecated
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGRenderingIntent
---
{{APIRef("SVG")}}{{deprecated_header}}

The **`SVGRenderingIntent`** interface defines the enumerated list of possible values for {{SVGAttr("rendering-intent")}} attributes or descriptors.

{{InheritanceDiagram}}

> **Warning:** This interface was removed in the SVG 2 specification.

## Constants

| Name                                     | Value | Description                                                                                                                                                  |
| ---------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `RENDERING_INTENT_UNKNOWN`               | 0     | The type is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| `RENDERING_INTENT_AUTO`                  | 1     | Corresponds to the value `auto`.                                                                                                                             |
| `RENDERING_INTENT_PERCEPTUAL`            | 2     | Corresponds to the value `perceptual`.                                                                                                                       |
| `RENDERING_INTENT_RELATIVE_COLORIMETRIC` | 3     | Corresponds to the value `relative-colorimetric`.                                                                                                            |
| `RENDERING_INTENT_SATURATION`            | 4     | Corresponds to the value `saturation`.                                                                                                                       |
| `RENDERING_INTENT_ABSOLUTE_COLORIMETRIC` | 5     | Corresponds to the value `absolute-colorimetric`.                                                                                                            |

## Properties

_This interface doesn't implement any specific properties._

## Methods

_This interface doesn't implement any specific methods._

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{SVGAttr("rendering-intent")}}
