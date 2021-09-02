---
title: FocusEvent.relatedTarget
slug: Web/API/FocusEvent/relatedTarget
tags:
  - API
  - Event
  - Experimental
  - FocusEvent
  - Property
  - Reference
browser-compat: api.FocusEvent.relatedTarget
---
{{ apiref("DOM Events") }}

The **`FocusEvent.relatedTarget`** read-only property is the
secondary target, depending on the type of event:

| Event name                   | `target`                                                 | `relatedTarget`                                                    |
| ---------------------------- | -------------------------------------------------------- | ------------------------------------------------------------------ |
| {{Event("blur")}}     | The {{domxref("EventTarget")}} losing focus    | The {{domxref("EventTarget")}} receiving focus (if any). |
| {{Event("focus")}}     | The {{domxref("EventTarget")}} receiving focus | The {{domxref("EventTarget")}} losing focus (if any)     |
| {{Event("focusin")}} | The {{domxref("EventTarget")}} receiving focus | The {{domxref("EventTarget")}} losing focus (if any)     |
| {{Event("focusout")}} | The {{domxref("EventTarget")}} losing focus    | The {{domxref("EventTarget")}} receiving focus (if any)  |

Note that [many elements can't have
focus](https://stackoverflow.com/a/42764495/1026), which is a common reason for `relatedTarget` to be
`null`. `relatedTarget` may also be set to `null` for
security reasons, like when tabbing in or out of a page.

{{domxref("MouseEvent.relatedTarget")}} is a similar property for mouse events.

## Syntax

```js
secondTarget = focusEvent.relatedTarget
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The {{domxref("FocusEvent")}} interface it belongs to.
