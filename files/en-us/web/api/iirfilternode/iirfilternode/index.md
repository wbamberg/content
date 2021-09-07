---
title: IIRFilterNode()
slug: Web/API/IIRFilterNode/IIRFilterNode
tags:
  - API
  - Audio
  - Constructor
  - IIRFilterNode
  - Media
  - Reference
  - Web Audio API
browser-compat: api.IIRFilterNode.IIRFilterNode
---
{{APIRef("Web Audio API")}}

The **`IIRFilterNode()`** constructor
of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("IIRFilterNode")}} object which an {{domxref("AudioNode")}} processor
which implements a general infinite impulse response filter.

## Syntax

```js
var iIRFilterNode = new IIRFilterNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : A reference to an {{domxref("AudioContext")}}.
- _options_

  - : Options are as follows:

    - `feedforward`: A sequence of feedforward coefficients.
    - `feedback`: A sequence of feedback coefficients.

Unlike other nodes in the Web Audio API, the options passed into the IIR
filter upon creation are not optional. The filter needs these values to work and with
the vast range of filters available, there is no default.

### Return value

A new {{domxref("IIRFilterNode")}} object instance.

## Examples

```js
let feedForward = [0.00020298, 0.0004059599, 0.00020298];
let feedBackward = [1.0126964558, -1.9991880801, 0.9873035442];

const AudioContext = window.AudioContext || window.webkitAudioContext;
const audioCtx = new AudioContext();

const iirFilter = new IIRFilterNode(audioCtx, { feedforward: feedForward, feedback: feedBackward });
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
