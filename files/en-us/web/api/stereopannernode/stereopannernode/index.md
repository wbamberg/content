---
title: StereoPannerNode()
slug: Web/API/StereoPannerNode/StereoPannerNode
tags:
  - API
  - Audio
  - Constructor
  - Media
  - Reference
  - StereoPannerNode
  - Web Audio API
browser-compat: api.StereoPannerNode.StereoPannerNode
---
{{APIRef("Web Audio API")}}

The **`StereoPannerNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("StereoPannerNode")}} object which is an {{domxref("AudioNode")}} that
represents a simple stereo panner node that can be used to pan an audio stream left or
right.

## Syntax

```js
var stereoPannerNode = StereoPannerNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : A reference to an {{domxref("AudioContext")}}.
- _options_ {{optional_inline}}

  - : Options are as follows:

    - `pan`: A floating point number in the range \[-1,1] indicating
      the position of an {{domxref("AudioNode")}} in an output image. The value
      \-1 represents full left and 1 represents full right. The default value is
      `0`.

### Return value

A new {{domxref("StereoPannerNode")}} object instance.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
