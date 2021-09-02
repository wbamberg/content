---
title: MediaStreamAudioDestinationNode()
slug: Web/API/MediaStreamAudioDestinationNode/MediaStreamAudioDestinationNode
tags:
  - API
  - Audio
  - Constructor
  - MediaStreamAudioDestinationNode
  - Reference
  - Web Audio API
browser-compat: api.MediaStreamAudioDestinationNode.MediaStreamAudioDestinationNode
---
{{APIRef("Web Audio API")}}

The **`MediaStreamAudioDestinationNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new {{domxref("MediaStreamAudioDestinationNode")}} object instance.

## Syntax

```js
var myAudioDest = new MediaStreamAudioDestinationNode(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : An {{domxref("AudioContext")}} representing the audio context you want the node to be associated with.
- _options {{optional_inline}}_
  - : An [`AudioNodeOptions`](https://webaudio.github.io/web-audio-api/#dictionary-audionodeoptions-members) dictionary object defining the properties you want the `MediaStreamAudioDestinationNode` to have.

### Return value

A new {{domxref("MediaStreamAudioDestinationNode")}} object instance.

## Example

```js
var ac = new AudioContext();

var myDestination = new MediaStreamAudioDestinationNode(ac);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
