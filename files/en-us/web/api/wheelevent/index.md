---
title: WheelEvent
slug: Web/API/WheelEvent
tags:
  - API
  - DOM
  - Interface
  - Reference
  - WheelEvent
browser-compat: api.WheelEvent
---
{{APIRef("DOM Events")}}

The **`WheelEvent`** interface represents events that occur due to the user moving a mouse wheel or similar input device.

> **Note:** This is the standard wheel event interface to use. Old versions of browsers implemented the non-standard and non-cross-browser-compatible {{DOMxRef("MouseWheelEvent")}} and {{DOMxRef("MouseScrollEvent")}} interfaces. Use this interface and avoid the non-standard ones.

> **Note:** Do not confuse the {{domxref("Element/wheel_event", "wheel")}} event with the {{domxref("Element/scroll_event", "scroll")}} event. The default action of a `wheel` event is implementation-defined. Thus, a `wheel` event doesn't necessarily dispatch a `scroll` event. Even when it does, that doesn't mean that the `delta*` values in the `wheel` event necessarily reflect the content's scrolling direction. Therefore, do not rely on `delta*` properties to get the content's scrolling direction. Instead, detect value changes to {{DOMxRef("Element.scrollLeft", "scrollLeft")}} and {{DOMxRef("Element.scrollTop", "scrollTop")}} of the target in the `scroll` event.

{{InheritanceDiagram}}

## Constructor

- {{DOMxRef("WheelEvent.WheelEvent", "WheelEvent()")}}
  - : Creates a `WheelEvent` object.

## Properties

_This interface inherits properties from its ancestors, {{DOMxRef("MouseEvent")}}, {{DOMxRef("UIEvent")}}, and {{DOMxRef("Event")}}._

- {{DOMxRef("WheelEvent.deltaX")}}{{ReadOnlyInline}}
  - : Returns a `double` representing the horizontal scroll amount.
- {{DOMxRef("WheelEvent.deltaY")}}{{ReadOnlyInline}}
  - : Returns a `double` representing the vertical scroll amount.
- {{DOMxRef("WheelEvent.deltaZ")}}{{ReadOnlyInline}}
  - : Returns a `double` representing the scroll amount for the z-axis.
- {{DOMxRef("WheelEvent.deltaMode")}}{{ReadOnlyInline}}

  - : Returns an `unsigned long` representing the unit of the `delta*` values' scroll amount. Permitted values are:

    <table class="standard-table">
      <thead>
        <tr>
          <td class="header">Constant</td>
          <td class="header">Value</td>
          <td class="header">Description</td>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code>WheelEvent.DOM_DELTA_PIXEL</code></td>
          <td><code>0x00</code></td>
          <td>The <code>delta*</code> values are specified in pixels.</td>
        </tr>
        <tr>
          <td><code>WheelEvent.DOM_DELTA_LINE</code></td>
          <td><code>0x01</code></td>
          <td>
            The <code>delta*</code> values are specified in lines. Each mouse click
            scrolls a line of content, where the method used to calculate line
            height is browser dependent.
          </td>
        </tr>
        <tr>
          <td><code>WheelEvent.DOM_DELTA_PAGE</code></td>
          <td><code>0x02</code></td>
          <td>
            The <code>delta*</code> values are specified in pages. Each mouse click
            scrolls a page of content.
          </td>
        </tr>
      </tbody>
    </table>

- {{DOMxRef("WheelEvent.wheelDelta")}}{{ReadOnlyInline}} {{deprecated_inline}}
  - : Returns an integer (32-bit) representing the distance in pixels.
- {{DOMxRef("WheelEvent.wheelDeltaX")}}{{ReadOnlyInline}} {{deprecated_inline}}
  - : Returns an integer representing the horizontal scroll amount.
- {{DOMxRef("WheelEvent.wheelDeltaY")}}{{ReadOnlyInline}} {{deprecated_inline}}
  - : Returns an integer representing the vertical scroll amount.

> **Note:** [Element: mousewheel event](/en-US/docs/Web/API/Element/mousewheel_event) has additional documentation about the deprecated properties `wheelDelta`, `wheelDeltaX`, `wheelDeltaY`.

## Methods

_This interface doesn't define any specific methods, but inherits methods from its ancestors, {{DOMxRef("MouseEvent")}}, {{DOMxRef("UIEvent")}}, and {{DOMxRef("Event")}}._

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("Element/wheel_event", "wheel")}} event
- Interfaces replaced by this one:

  - Gecko's legacy mouse wheel event object: {{DOMxRef("MouseScrollEvent")}}
  - Non-gecko browsers' legacy mouse wheel event object: {{DOMxRef("MouseWheelEvent")}}
