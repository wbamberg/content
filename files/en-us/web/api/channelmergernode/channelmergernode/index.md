---
title: ChannelMergerNode()
slug: Web/API/ChannelMergerNode/ChannelMergerNode
tags:
  - API
  - Audio
  - ChannelMergerNode
  - Constructor
  - Reference
  - Web Audio API
browser-compat: api.ChannelMergerNode.ChannelMergerNode
---
{{APIRef("Web Audio API")}}

The **`ChannelMergerNode()`** constructor creates a new {{domxref("ChannelMergerNode")}} object instance.

## Syntax

    var myNode = new ChannelMergerNode(context, options);

### Parameters

- _context_
  - : A {{domxref("BaseAudioContext")}} representing the audio context you want the node to be associated with.
- _options_ {{optional_inline}}

  - : A [`ChannelMergerOptions`](https://webaudio.github.io/web-audio-api/#idl-def-ChannelMergerOptions) dictionary object defining the properties you want the `ChannelMergerNode` to have (also inherits parameters from the {{domxref("AudioNodeOptions")}} dictionary):

    - `numberOfInputs`: A number defining the number of inputs the {{domxref("ChannelMergerNode")}} should have. If not specified, the default value used is 6.

### Return value

A new {{domxref("ChannelMergerNode")}} object instance.

### Exceptions

- `InvalidStateError`
  - : An option such as `channelCount` or `channelCountMode` has been given an invalid value.

## Example

    var ac = new AudioContext();

    var options = {
      numberOfInputs : 2
    }

    var myMerger = new ChannelMergerNode(ac, options);

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
