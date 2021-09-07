---
title: MouseEvent.which
slug: Web/API/MouseEvent/which
tags:
  - API
  - DOM Events
  - MouseEvent
  - Non-standard
  - Property
  - Read-only
  - Reference
browser-compat: api.MouseEvent.which
---
{{APIRef("DOM Events")}}

{{Non-standard_header}}

The **`MouseEvent.which`** read-only property indicates which
button was pressed on the mouse to trigger the event. The standard alternatives to this
property are {{ domxref("MouseEvent.button") }} and {{ domxref("MouseEvent.buttons") }}.

## Syntax

```js
var buttonPressed = instanceOfMouseEvent.which
```

### Return value

A number representing a given button:

- `0`: No button
- `1`: Left button
- `2`: Middle button (if present)
- `3`: Right button

For a mouse configured for left-handed use, the button actions are reversed. In this
case, the values are read from right to left.

## Specifications

This is not part of any specification.

## Browser compatibility

{{Compat}}

## See also

- {{ domxref("MouseEvent") }}
