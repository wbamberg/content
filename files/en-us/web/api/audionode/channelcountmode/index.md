---
title: AudioNode.channelCountMode
slug: Web/API/AudioNode/channelCountMode
tags:
  - API
  - AudioNode
  - Property
  - Reference
  - Web Audio API
  - channelCountMode
browser-compat: api.AudioNode.channelCountMode
---
{{ APIRef("Web Audio API") }}

The `channelCountMode` property of the {{ domxref("AudioNode") }} interface represents an enumerated value describing the way channels must be matched between the node's inputs and outputs.

The possible values of `channelCountMode` and their meanings are:

| Value         | Description                                                                                                                                               | The following `AudioNode` children default to this value                                                                                                                                                                                           |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `max`         | The number of channels is equal to the maximum number of channels of all connections. In this case, `channelCount` is ignored and only up-mixing happens. | {{domxref("GainNode")}}, {{domxref("DelayNode")}}, {{domxref("ScriptProcessorNode")}}, {{domxref("ChannelMergerNode")}}, {{domxref("BiquadFilterNode")}}, {{domxref("WaveShaperNode")}} |
| `clamped-max` | The number of channels is equal to the maximum number of channels of all connections, _clamped_ to the value of `channelCount`.                           | {{domxref("PannerNode")}}, {{domxref("ConvolverNode")}}, {{domxref("DynamicsCompressorNode")}}                                                                                                                           |
| `explicit`    | The number of channels is defined by the value of `channelCount`.                                                                                         | {{domxref("AudioDestinationNode")}}, {{domxref("AnalyserNode")}}, {{domxref("ChannelSplitterNode")}}                                                                                                               |

> **Note:** In older versions of the spec, the default for a {{domxref("ChannelSplitterNode")}} was max.

## Syntax

```js
var oscillator = audioCtx.createOscillator();
oscillator.channelCountMode = 'explicit';
```

### Value

A enumerated value representing a [channelCountMode](https://webaudio.github.io/web-audio-api/#idl-def-ChannelCountMode).

## Example

```js
var AudioContext = window.AudioContext || window.webkitAudioContext;

var audioCtx = new AudioContext();

var oscillator = audioCtx.createOscillator();
var gainNode = audioCtx.createGain();

oscillator.connect(gainNode);
gainNode.connect(audioCtx.destination);

oscillator.channelCountMode = 'explicit';
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using the Web Audio API](/en-US/docs/Web/API/Web_Audio_API/Using_Web_Audio_API)
