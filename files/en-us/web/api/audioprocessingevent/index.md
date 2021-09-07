---
title: AudioProcessingEvent
slug: Web/API/AudioProcessingEvent
tags:
  - API
  - Deprecated
  - Interface
  - Internationalization
  - Reference
  - Web Audio API
browser-compat: api.AudioProcessingEvent
---
{{APIRef("Web Audio API")}}{{deprecated_header}}

The [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) `AudioProcessingEvent` represents events that occur when a {{domxref("ScriptProcessorNode")}} input buffer is ready to be processed.

> **Note:** As of the August 29 2014 Web Audio API spec publication, this feature has been marked as deprecated, and is soon to be replaced by [AudioWorklet](https://webaudio.github.io/web-audio-api/#audioworklet).

## Properties

_The list below includes the properties inherited from its parent, {{domxref("Event")}}_.

| Property                                | Type                                 | Description                                                                                                                                                                                                                                                                                                                                                                             |
| --------------------------------------- | ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `target` {{ReadOnlyInline}}       | {{domxref("EventTarget")}} | The event target (the topmost target in the DOM tree).                                                                                                                                                                                                                                                                                                                                  |
| `type` {{ReadOnlyInline}}         | {{domxref("DOMString")}}     | The type of event.                                                                                                                                                                                                                                                                                                                                                                      |
| `bubbles` {{ReadOnlyInline}}      | `boolean`                            | Does the event normally bubble?                                                                                                                                                                                                                                                                                                                                                         |
| `cancelable` {{ReadOnlyInline}}   | `boolean`                            | Is it possible to cancel the event?                                                                                                                                                                                                                                                                                                                                                     |
| `playbackTime` {{ReadOnlyInline}} | `double`                             | The time when the audio will be played, as defined by the time of {{domxref("BaseAudioContext/currentTime", "AudioContext.currentTime")}}                                                                                                                                                                                                                      |
| `inputBuffer` {{ReadOnlyInline}}  | {{domxref("AudioBuffer")}} | The buffer containing the input audio data to be processed. The number of channels is defined as a parameter, `numberOfInputChannels`, of the factory method {{domxref("BaseAudioContext/createScriptProcessor", "AudioContext.createScriptProcessor()")}}. Note the returned `AudioBuffer` is only valid in the scope of the `onaudioprocess` function. |
| `outputBuffer` {{ReadOnlyInline}} | {{domxref("AudioBuffer")}} | The buffer where the output audio data should be written. The number of channels is defined as a parameter, `numberOfOutputChannels`, of the factory method {{domxref("BaseAudioContext/createScriptProcessor", "AudioContext.createScriptProcessor()")}}. Note the returned `AudioBuffer` is only valid in the scope of the `onaudioprocess` function.  |

## Example

See [`BaseAudioContext.createScriptProcessor()`](/en-US/docs/Web/API/BaseAudioContext/createScriptProcessor#example) for example code that uses an `AudioProcessingEvent`.

## Browser compatibility

{{Compat}}

## See also

- [Using the Web Audio API](/en-US/docs/Web/API/Web_Audio_API/Using_Web_Audio_API)
