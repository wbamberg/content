---
title: DelayNode()
slug: Web/API/DelayNode/DelayNode
tags:
  - API
  - Audio
  - Constructor
  - DelayNode
  - Media
  - Reference
  - Web Audio API
browser-compat: api.DelayNode.DelayNode
---
{{APIRef("Web Audio API")}}

The **`DelayNode()`**
constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API)
creates a new {{domxref("DelayNode")}} object with a delay-line; an AudioNode
audio-processing module that causes a delay between the arrival of an input data, and
its propagation to the output.

## Syntax

```js
var delayNode = new DelayNode(context);
var delayNode = new DelayNode(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary._

- _context_
  - : A reference to an {{domxref("AudioContext")}} or {{domxref("OfflineAudioContext")}}.
- _options_ {{optional_inline}}

  - : An object specifying the delay node options. Can contain the following members:

    - `delayTime`: The initial delay time for the node, in seconds. The
      default is `0`.
    - `maxDelayTime`: The maximum delay time for the node, in seconds.
      Defaults to `1`.

### Return value

A new {{domxref("DelayNode")}} object instance.

## Example

```js
const audioCtx = new AudioContext();
const delayNode = new DelayNode(audioCtx, {
  delayTime: 0.5,
  maxDelayTime: 2,
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
