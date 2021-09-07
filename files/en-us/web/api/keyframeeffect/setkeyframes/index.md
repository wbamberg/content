---
title: KeyframeEffect.setKeyframes()
slug: Web/API/KeyframeEffect/setKeyframes
tags:
  - API
  - Animations
  - Experimental
  - KeyframeEffect
  - Method
  - Reference
  - setKeyframes
  - waapi
  - web animations api
browser-compat: api.KeyframeEffect.setKeyframes
---
{{ SeeCompatTable() }}{{ APIRef("Web Animations API") }}

The **`setKeyframes()`** method of the {{domxref("KeyframeEffect")}} interface replaces the keyframes that make up the affected `KeyframeEffect` with a new set of keyframes.

## Syntax

```js
existingKeyframeEffect.setKeyframes(keyframes);
```

### Parameters

- keyframes

  - : A keyframe object or `null`. If set to `null`, the keyframes are replaced with a sequence of empty keyframes.

    More information about a keyframe object's [format](/en-US/docs/Web/API/Web_Animations_API/Keyframe_Formats#syntax).

### Return value

Void.

### Exceptions

| Exception   | Explanation                                                                                                                                                                                                                                              |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `TypeError` | One or more of the frames were not of the correct type of object, the keyframes were not [loosely sorted by offset](https://w3c.github.io/web-animations/#loosely-sorted-by-offset), or a keyframe existed with an offset of less than 0 or more than 1. |

> **Note:** If the keyframes cannot be processed or are malformed, the `KeyframeEffect`'s keyframes are not modified.

## Examples

```js
// passing an array of keyframe objects
existingKeyframeEffect.setKeyframes(
[
  { color: 'blue' },
    { color: 'green', left: '10px' }
  ]
);

// passing an object with arrays for values
existingKeyframeEffect.setKeyframes(
  {
    color: ['blue', 'green'],
    left: [ '0', '10px']
  }
);

// passing a single-member object
existingKeyframeEffect.setKeyframes(
  {
    color: 'blue'
  }
);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [KeyframeEffect Interface](/en-US/docs/Web/API/KeyframeEffect)
- [Web Animations API](/en-US/docs/Web/API/Web_Animations_API)
