---
title: WheelEvent.deltaMode
slug: Web/API/WheelEvent/deltaMode
tags:
  - API
  - DOM
  - Property
  - Read-only
  - Reference
  - WheelEvent
browser-compat: api.WheelEvent.deltaMode
---
{{APIRef("DOM Events")}}

The **`WheelEvent.deltaMode`** read-only property returns an
`unsigned long` representing the unit of the delta values scroll amount.
Permitted values are:

<table class="standard-table">
  <tbody>
    <tr>
      <td class="header">Constant</td>
      <td class="header">Value</td>
      <td class="header">Description</td>
    </tr>
    <tr>
      <td><code>DOM_DELTA_PIXEL</code></td>
      <td><code>0x00</code></td>
      <td>The delta values are specified in pixels.</td>
    </tr>
    <tr>
      <td><code>DOM_DELTA_LINE</code></td>
      <td><code>0x01</code></td>
      <td>The delta values are specified in lines.</td>
    </tr>
    <tr>
      <td><code>DOM_DELTA_PAGE</code></td>
      <td><code>0x02</code></td>
      <td>The delta values are specified in pages.</td>
    </tr>
  </tbody>
</table>

## Syntax

```js
var unit = event.deltaMode;
```

## Example

```js
var syntheticEvent = new WheelEvent("syntheticWheel", {"deltaX": 4, "deltaMode": 0});

console.log(syntheticEvent.deltaMode);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{ event("wheel") }}
- {{domxref("WheelEvent")}}
