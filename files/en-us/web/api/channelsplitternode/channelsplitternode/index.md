---
title: ChannelSplitterNode()
slug: Web/API/ChannelSplitterNode/ChannelSplitterNode
tags:
  - API
  - Audio
  - ChannelSplitterNode
  - Constructor
  - Reference
  - Splitter
  - Web Audio
  - Web Audio API
browser-compat: api.ChannelSplitterNode.ChannelSplitterNode
---
{{APIRef("Web Audio API")}}

The **`ChannelSplitterNode()`** constructor of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) creates a new {{domxref("ChannelSplitterNode")}} object instance, representing a node that splits the input into a separate output for each of the source node's audio channels.

## Syntax

```js
var splitter = new ChannelSpitterNode(context, options);
```

### Parameters

_Inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary_.

- `context`
  - : A {{domxref("BaseAudioContext")}} representing the audio context you want the node to be associated with.
- `options` {{optional_inline}}

  - : A [`ChannelSplitterOptions`](https://webaudio.github.io/web-audio-api/#idl-def-ChannelSplitterOptions) dictionary object defining the properties you want the `ChannelSplitterNode` to have (It also inherits the options defined in the [`AudioNodeOptions`](https://webaudio.github.io/web-audio-api/#idl-def-AudioNodeOptions) dictionary):

    - `numberOfOutputs`: A number defining the number of inputs the {{domxref("ChannelSplitterNode")}} should have. If not specified, the default value used is 6.

### Return value

A new {{domxref("ChannelSplitterNode")}} object instance.

## Example

```js
var ac = new AudioContext();

var options = {
  numberOfOutputs : 2
}

var mySplitter = new ChannelSplitterNode(ac, options);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
