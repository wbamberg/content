---
title: EffectTiming.duration
slug: Web/API/EffectTiming/duration
tags:
  - API
  - Animation
  - EffectTiming
  - Experimental
  - KeyframeEffect
  - Property
  - Reference
  - Web Animations
  - animate
  - duration
  - waapi
  - web animations api
browser-compat: api.EffectTiming.duration
---
{{ SeeCompatTable() }}{{ APIRef("Web Animations") }}

The **`duration`** property of the dictionary
{{domxref("EffectTiming")}} in the [Web
Animations API](/en-US/docs/Web/API/Web_Animations_API) specifies the duration in milliseconds that a single iteration
(from beginning to end) the animation should take to complete.

> **Note:** {{domxref("Element.animate()")}},
> {{domxref("KeyframeEffectReadOnly.KeyframeEffectReadOnly",
    "KeyframeEffectReadOnly()")}}, and {{domxref("KeyframeEffect.KeyframeEffect",
    "KeyframeEffect()")}} all accept an object of timing properties including
> `duration`. The value of `duration` corresponds directly
> to {{domxref("AnimationEffectTimingReadOnly.duration")}} in
> {{domxref("AnimationEffectReadOnly.timing", "timing")}} objects returned by
> {{domxref("AnimationEffectReadOnly")}}, {{domxref("KeyframeEffectReadOnly")}}, and
> {{domxref("KeyframeEffect")}}.

## Syntax

```js
var timingProperties = {
  duration: durationInMilliseconds | "auto"
};

timingProperties.duration = durationInMilliseconds | "auto";
```

### Value

The number of milliseconds long a single beginning-to-end iteration of the animation
should take. The default is `"auto"`. This value must not be negative;
otherwise, it can have any value (including positive infinity).

> **Note:** Currently, a value of `"auto"` is the same as specifying 0.0. This is a
> forwards-compatibility measure since in the future, "auto" will be expanded to take
> into account the duration of any child effects. Consider using `"auto"`
> rather than 0 if that makes sense.

### Exceptions

- `TypeError`
  - : The specified value is either a string other than `"auto"`, a number less
    than zero, {{jsxref("NaN")}}, or some other type of object entirely.

## Examples

In the [Pool of
Tears](http://codepen.io/rachelnabors/pen/EPJdJx?editors=0010) example, each tear is passed a random `duration` via its timing
object:

```js
// Randomizer function
var getRandomMsRange = function(min, max) {
  return Math.random() * (max - min) + min;
}

// Loop through each tear
tears.forEach(function(el) {

  // Animate each tear
  el.animate(
    tearsFalling,
    {
       delay: getRandomMsRange(-1000, 1000), // randomized for each tear
       duration: getRandomMsRange(2000, 6000), // randomized for each tear
       iterations: Infinity,
       easing: "cubic-bezier(0.6, 0.04, 0.98, 0.335)"
    });
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Web Animations API](/en-US/docs/Web/API/Web_Animations_API)
- {{domxref("Element.animate()")}},
  {{domxref("KeyframeEffectReadOnly.KeyframeEffectReadOnly",
    "KeyframeEffectReadOnly()")}}, and {{domxref("KeyframeEffect.KeyframeEffect",
    "KeyframeEffect()")}} all accept an object of timing properties including this one.
- The value of this property corresponds to property of the same name in
  {{domxref("AnimationEffectReadOnly.timing")}},
  {{domxref("KeyframeEffectReadOnly.timing")}},
  and {{domxref("KeyframeEffect.timing")}}).
- CSS's {{cssxref("transition-duration")}} and {{cssxref("animation-duration")}}
  properties
