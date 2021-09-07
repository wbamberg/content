---
title: GainNode()
slug: Web/API/GainNode/GainNode
tags:
  - API
  - Audio
  - Constructor
  - GainNode
  - Media
  - Reference
  - Web Audio API
browser-compat: api.GainNode.GainNode
---
{{APIRef("Web Audio API")}}

The **`GainNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new
{{domxref("GainNode")}} object which is an {{domxref("AudioNode")}} that represents a
change in volume.

## Syntax

```js
var gainNode = new GainNode(context, options)
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- `context`
  - : A reference to a {{domxref("BaseAudioContext")}}, e.g. an {{domxref("AudioContext")}}.
- `options` {{optional_inline}}

  - : Options are as follows:

    - `gain`: The amount of gain to apply. This parameter is a-rate
      and it's nominal range is (-∞,+∞). The default is `1`.

### Return value

A new {{domxref("GainNode")}} object instance.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
