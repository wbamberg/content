---
title: AudioNodeOptions
slug: Web/API/AudioNodeOptions
tags:
  - API
  - Audio
  - AudioNodeOptions
  - Dictionary
  - Interface
  - Options
  - Reference
  - Web Audio API
browser-compat: api.AudioNodeOptions
---
{{APIRef("'Web Audio API'")}}

The **`AudioNodeOptions`** dictionary
of the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) specifies options
that can be used when creating new {{domxref("AudioNode")}} objects.

`AudioNodeOptions` is inherited from by the option objects of the different
types of audio node constructors. See for example
{{domxref("AnalyserNode.AnalyserNode")}} or {{domxref("GainNode.GainNode")}}.

## Syntax

```js
var audioNodeOptions = {
  "channelCount" : 2,
  "channelCountMode" : "max",
  "channelInterpretation" : "discrete"
}
```

### Properties

- `channelCount` {{optional_inline}}
  - : Represents an integer used to determine how many channels are used when [up-mixing
    and down-mixing](/en-US/docs/Web/API/Web_Audio_API/Basic_concepts_behind_Web_Audio_API#up-mixing_and_down-mixing) connections to any inputs to the node. (See
    {{domxref("AudioNode.channelCount")}} for more information.) Its usage and precise
    definition depend on the value of {{domxref("AudioNodeOptions.channelCountMode")}}.
- `channelCountMode` {{optional_inline}}
  - : Represents an enumerated value describing the way channels must be matched between
    the node's inputs and outputs. (See {{domxref("AudioNode.channelCountMode")}} for more
    information including default values.)
- `channelInterpretation` {{optional_inline}}
  - : Represents an enumerated value describing the meaning of the channels. This
    interpretation will define how audio [up-mixing
    and down-mixing](/en-US/docs/Web/API/Web_Audio_API/Basic_concepts_behind_Web_Audio_API#up-mixing_and_down-mixing) will happen.
    The possible values are `"speakers"` or `"discrete"`. (See
    {{domxref("AudioNode.channelCountMode")}} for more information including default
    values.)

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
