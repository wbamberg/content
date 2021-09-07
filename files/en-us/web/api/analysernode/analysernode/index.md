---
title: AnalyserNode()
slug: Web/API/AnalyserNode/AnalyserNode
tags:
  - API
  - AnalyserNode
  - Audio
  - Constructor
  - Media
  - Reference
  - Web Audio API
browser-compat: api.AnalyserNode.AnalyserNode
---
{{APIRef("'Web Audio API'")}}

The **`AnalyserNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new {{domxref("AnalyserNode")}} object instance.

## Syntax

```js
var analyserNode = new AnalyserNode(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary._

- _context_
  - : A reference to an {{domxref("AudioContext")}} or {{domxref("OfflineAudioContext")}}.
- _options_ {{optional_inline}}

  - : An object with the following properties, all optional:

    - **`fftSize`**: The desired initial size of the [FFT](https://en.wikipedia.org/wiki/Fast_Fourier_transform) for [frequency-domain](https://en.wikipedia.org/wiki/Frequency_domain) analysis. 
      The default is `2048`.
    - **`maxDecibels`**: The desired initial maximum power in [dB](https://en.wikipedia.org/wiki/Decibel) for FFT analysis.
      The default is `-30`.
    - **`minDecibels`**: The desired initial minimum power in dB for FFT analysis.
      The default is `-100`.
    - **`smoothingTimeConstant`**: The desired initial smoothing constant for the FFT analysis. The default is `0.8`.

### Return value

A new {{domxref("AnalyserNode")}} object instance.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("BaseAudioContext.createAnalyser()")}}, the equivalent factory method
