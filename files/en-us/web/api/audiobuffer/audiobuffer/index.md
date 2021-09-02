---
title: AudioBuffer()
slug: Web/API/AudioBuffer/AudioBuffer
tags:
  - API
  - Audio
  - AudioBuffer
  - Buffer
  - Constructor
  - Media
  - Reference
  - Web Audio
  - Web Audio API
  - sound
browser-compat: api.AudioBuffer.AudioBuffer
---
{{APIRef("Web Audio API")}}

The **`AudioBuffer`** constructor of
the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("AudioBuffer")}} object.

## Syntax

```js
var audioBuffer = new AudioBuffer(options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- `options`

  - : Options are as follows:

    - `length`: The size of the audio buffer in sample-frames. To determine
      the `length` to use for a specific number of seconds of audio, use
      `numSeconds * sampleRate`.
    - `numberOfChannels`: The number of channels for the buffer. The
      default is 1, and all user agents are required to support at least 32 channels.
    - `sampleRate`: The sample rate in Hz for the buffer. The default is
      the sample rate of the `context` used in constructing this object. User
      agents are required to support sample rates from 8,000 Hz to 96,000 Hz (but are
      allowed to go farther outside this range).

#### Deprecated parameters

- `context` {{Deprecated_Inline}}
  - : A reference to an {{domxref("AudioContext")}}. This parameter was removed from the
    spec.

### Return value

A new {{domxref("AudioBuffer")}} object instance.

### Exceptions

- `NotSupportedError`
  - : One or more of the options are negative or otherwise has an invalid value (such as
    `numberOfChannels` being higher than supported, or a
    `sampleRate` outside the nominal range).
- `RangeError`
  - : There isn't enough memory available to allocate the buffer.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
