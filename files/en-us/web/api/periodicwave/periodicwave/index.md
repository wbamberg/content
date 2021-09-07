---
title: PeriodicWave()
slug: Web/API/PeriodicWave/PeriodicWave
tags:
  - API
  - Audio
  - Constructor
  - PeriodicWave
  - Reference
  - Web Audio API
browser-compat: api.PeriodicWave.PeriodicWave
---
{{APIRef("Web Audio API")}}

The **`PeriodicWave()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("PeriodicWave")}} object instance.

## Syntax

```js
var myWave = new PeriodicWave(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- `context`
  - : A {{domxref("BaseAudioContext")}} representing the audio context you want the node
    to be associated with.
- `options` {{optional_inline}}

  - : A
    [`PeriodicWaveOptions`](https://webaudio.github.io/web-audio-api/#idl-def-PeriodicWaveOptions)
    dictionary object defining the properties you want the `PeriodicWave` to
    have (It also inherits the options defined in the [PeriodicWaveConstraints](https://webaudio.github.io/web-audio-api/#idl-def-PeriodicWaveConstraints)
    dictionary.):

    - `real`: A {{jsxref("Float32Array")}} containing the cosine terms
      that you want to use to form the wave (equivalent to the `real`
      parameter of {{domxref("BaseAudioContext.createPeriodicWave")}}).
    - `imag`: A {{jsxref("Float32Array")}} containing the sine terms that
      you want to use to form the wave (equivalent to the `imag` parameter of
      {{domxref("BaseAudioContext.createPeriodicWave")}}).

### Return value

A new {{domxref("PeriodicWave")}} object instance.

## Example

```js
var real = new Float32Array(2);
var imag = new Float32Array(2);
var ac = new AudioContext();

real[0] = 0;
imag[0] = 0;
real[1] = 1;
imag[1] = 0;

var options = {
  real : real,
  imag : imag,
  disableNormalization : false
}

var wave = new PeriodicWave(ac, options);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
