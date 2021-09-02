---
title: MouseScrollEvent
slug: Web/API/MouseScrollEvent
tags:
  - API
  - DOM
  - DOM Events
  - Deprecated
  - Event
  - Interface
  - Reference
browser-compat: api.MouseScrollEvent
---
{{APIRef("DOM Events")}}{{ non-standard_header() }}{{deprecated_header}}

The **`MouseScrollEvent`** interface represents events that occur due to the user moving a mouse wheel or similar input device.

> **Warning:** Do not use this interface for wheel events.
>
> Like {{domxref("MouseWheelEvent")}}, this interface is non-standard and deprecated. It was used in Gecko-based browsers only. Instead use the standard _{{domxref("WheelEvent")}}._

## Method overview

<table class="standard-table">
  <tbody>
    <tr>
      <td>
        <code
          >void
          <a
            href="/en-US/docs/XPCOM_Interface_Reference/nsIDOMMouseScrollEvent#initMouseScrollEvent%28%29"
            >initMouseScrollEvent</a
          >(in DOMString typeArg, in boolean canBubbleArg, in boolean
          cancelableArg, in nsIDOMAbstractView viewArg, in long detailArg, in
          long screenXArg, in long screenYArg, in long clientXArg, in long
          clientYArg, in boolean ctrlKeyArg, in boolean altKeyArg, in boolean
          shiftKeyArg, in boolean metaKeyArg, in unsigned short buttonArg, in
          nsIDOMEventTarget relatedTargetArg, in long axis);</code
        >
      </td>
    </tr>
  </tbody>
</table>

## Attributes

<table class="standard-table">
  <tbody>
    <tr>
      <td class="header">Attribute</td>
      <td class="header">Type</td>
      <td class="header">Description</td>
    </tr>
    <tr>
      <td><code>axis</code> {{ReadOnlyInline}}</td>
      <td><code>long</code></td>
      <td>Indicates scroll direction.</td>
    </tr>
  </tbody>
</table>

## Constants

### Delta modes

<table class="standard-table">
  <tbody>
    <tr>
      <td class="header">Constant</td>
      <td class="header">Value</td>
      <td class="header">Description</td>
    </tr>
    <tr>
      <td><code>HORIZONTAL_AXIS</code></td>
      <td><code>0x01</code></td>
      <td>The event is caused by horizontal wheel operation.</td>
    </tr>
    <tr>
      <td><code>VERTICAL_AXIS</code></td>
      <td><code>0x02</code></td>
      <td>The event is caused by vertical wheel operation.</td>
    </tr>
  </tbody>
</table>

## Methods

- `initMouseScrollEvent()`
  - : See [nsIDOMMouseScrollEvent::initMouseScrollEvent()](/en-US/docs/XPCOM_Interface_Reference/nsIDOMMouseScrollEvent#initMouseScrollEvent%28%29).

## Browser compatibility

{{Compat}}

## See also

- `DOMMouseScroll`
- `MozMousePixelScroll`
- Non-gecko browsers' legacy mouse wheel event object: {{ domxref("MouseWheelEvent") }}
- Standardized mouse wheel event object: {{ domxref("WheelEvent") }}
