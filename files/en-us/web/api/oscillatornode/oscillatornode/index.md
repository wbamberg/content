---
title: OscillatorNode()
slug: Web/API/OscillatorNode/OscillatorNode
tags:
  - Audio
  - Constructor
  - Media
  - OscillatorNode
  - Reference
  - Web Audio
  - Web Audio API
browser-compat: api.OscillatorNode.OscillatorNode
---
{{APIRef("Web Audio API")}}

The **`OscillatorNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("OscillatorNode")}} object which is an {{domxref("AudioNode")}} that
represents a periodic waveform, like a sine wave, optionally setting the node's
properties' values to match values in a specified object.

If the default values of the properties are acceptable, you can optionally use the
{{domxref("BaseAudioContext.createOscillator()")}} factory method instead; see
[Creating an AudioNode](/en-US/docs/Web/API/AudioNode#creating_an_audionode).

## Syntax

```js
var oscillatorNode = new OscillatorNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- `context`
  - : A reference to an {{domxref("AudioContext")}}.
- `options` {{optional_inline}}

  - : An object whose properties specify the initial values for the oscillator node's
    properties. Any properties omitted from the object will take on the default value
    as documented.

    - `type`
      - : The shape of the wave produced by the node. Valid values are
        '`sine`', '`square`', '`sawtooth`',
        '`triangle`' and '`custom`'. The default is
        '`sine`'.
    - `detune`
      - : A detuning value (in cents) which will offset
        the `frequency` by the given amount. Its default is 0.
    - `frequency`
      - : The frequency (in {{interwiki("wikipedia", "hertz")}}) of the periodic
        waveform. Its default is 440.
    - `periodicWave`
      - : An arbitrary period waveform described by a {{domxref("PeriodicWave")}}
        object.

### Return value

A new {{domxref("OscillatorNode")}} object instance.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
