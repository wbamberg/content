---
title: MediaElementAudioSourceNode()
slug: Web/API/MediaElementAudioSourceNode/MediaElementAudioSourceNode
tags:
  - API
  - Audio
  - Constructor
  - MediaElementAudioSourceNode
  - Reference
  - Web Audio API
browser-compat: api.MediaElementAudioSourceNode.MediaElementAudioSourceNode
---
{{APIRef("Web Audio API")}}

The **`MediaElementAudioSourceNode()`** constructor creates a new {{domxref("MediaElementAudioSourceNode")}} object instance.

## Syntax

```js
var myAudioSource = new MediaElementAudioSourceNode(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- _context_
  - : An {{domxref("AudioContext")}} representing the audio context you want the node to be associated with.
- _options_

  - : A `MediaElementAudioSourceOptions` dictionary object defining the properties you want the `MediaElementAudioSourceNode` to have:

    - `mediaElement`: An {{domxref("HTMLMediaElement")}} that will be used as the source for the audio.

### Return value

A new {{domxref("MediaElementAudioSourceNode")}} object instance.

## Example

```js
var ac = new AudioContext();
var mediaElement = document.createElement('audio');

var options = {
  mediaElement : mediaElement
}

var myAudioSource = new MediaElementAudioSourceNode(ac, options);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
