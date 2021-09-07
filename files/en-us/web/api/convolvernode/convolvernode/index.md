---
title: ConvolverNode()
slug: Web/API/ConvolverNode/ConvolverNode
tags:
  - API
  - Audio
  - Constructor
  - Convolver
  - Reference
  - Web Audio API
browser-compat: api.ConvolverNode.ConvolverNode
---
{{APIRef("Web Audio API")}}

The **`ConvolverNode()`** constructor
of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("ConvolverNode")}} object instance.

## Syntax

```js
var convolverNode = new ConvolverNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : A reference to an {{domxref("AudioContext")}}.
- _options_ {{optional_inline}}

  - : Options are as follows:

    - `audioBuffer`: A mono, stereo, or
      4-channel *{{domxref("AudioBuffer")}}* containing the
      (possibly multichannel) impulse response used by the `ConvolverNode`
      to create the reverb effect.
    - `disableNormalization`: A boolean value controlling
      whether the impulse response from the buffer will be scaled by an equal-power
      normalization, or not. The default is '`false`'.

### Return value

A new {{domxref("ConvolverNode")}} object instance.

### Exceptions

| Exception           | Explanation                                                                                                                                                                                 |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `NotSupportedError` | The referenced {{domxref("AudioBuffer")}} does not have the correct number of channels, or it has a different sample rate to the associated {{domxref("AudioContext")}}. |

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
