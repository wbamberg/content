---
title: WaveShaperNode()
slug: Web/API/WaveShaperNode/WaveShaperNode
tags:
  - API
  - Audio
  - Constructor
  - Media
  - Reference
  - WaveShaperNode
  - Web Audio API
browser-compat: api.WaveShaperNode.WaveShaperNode
---
{{APIRef("Web Audio API")}}

The **`WaveShaperNode()`** constructor
of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("WaveShaperNode")}} object which is an {{domxref("AudioNode")}} that
represents a non-linear distorter.

## Syntax

```js
var waveShaperNode = new WaveShaperNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : A reference to an {{domxref("AudioContext")}}.
- _options_ {{optional_inline}}

  - : Options are as follows:

    - `curve`: The shaping curve used for the waveshaping effect. The input
      signal is nominally within the range \[-1;1].
    - `oversample`: Specifies what type of oversampling (if any) should be
      used when applying the shaping curve. Valid values are '`none`',
      '`2x`', or '`4x`'. The default is '`none`'.

### Return value

A new {{domxref("WaveShaperNode")}} object instance.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
