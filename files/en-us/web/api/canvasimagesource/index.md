---
title: CanvasImageSource
slug: Web/API/CanvasImageSource
tags:
  - API
  - Canvas
  - Helper
  - Reference
---
{{APIRef("Canvas API")}}

**`CanvasImageSource`** provides a mechanism for other interfaces to be used as image sources for some methods of the {{domxref("CanvasDrawImage")}} and {{domxref("CanvasFillStrokeStyles")}} interfaces. It’s just an internal helper type to simplify the specification. It’s not an interface and there are no objects implementing it.

The interfaces that it allows to be used as image sources are the following:

- {{domxref("HTMLImageElement")}}
- {{domxref("SVGImageElement")}}
- {{domxref("HTMLVideoElement")}}
- {{domxref("HTMLCanvasElement")}}
- {{domxref("ImageBitmap")}}
- {{domxref("OffscreenCanvas")}}

## Specifications

| Specification                                                                                                    | Status                           | Comment             |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------- |
| {{SpecName('HTML WHATWG', "scripting.html#canvasimagesource", "CanvasImageSource")}} | {{Spec2('HTML WHATWG')}} | Initial definition. |
