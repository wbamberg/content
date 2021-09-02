---
title: CSSPrimitiveValue.setFloatValue()
slug: Web/API/CSSPrimitiveValue/setFloatValue
tags:
  - API
  - CSSPrimitiveValue
  - Method
  - NeedsExample
  - setFloatValue
  - Deprecated
browser-compat: api.CSSPrimitiveValue.setFloatValue
---
{{APIRef("CSSOM")}}{{deprecated_header}}

The **`setFloatValue()`** method of the
{{domxref("CSSPrimitiveValue")}} interface is used to set a float value. If the property
attached to this value can't accept the specified unit or the float value, the value
will be unchanged and a {{domxref("DOMException")}} will be raised.

> **Note:** This method was part of an attempt to create a typed CSS Object Model. This attempt has been abandoned, and most browsers do
> not implement it.
>
> To achieve your purpose, you can use:
>
> - the untyped [CSS Object Model](/en-US/docs/Web/API/CSS_Object_Model), widely supported, or
> - the modern [CSS Typed Object Model API](/en-US/docs/Web/API/CSS_Typed_OM_API), less supported and considered experimental.

## Syntax

```js
cssPrimitiveValue.setFloatValue(unitType, floatValue);
```

### Parameters

- unitType

  - : An `unsigned short` representing the code for the unit type, in which the
    value should be returned. Valid values are:

    <table class="standard-table">
      <tbody>
        <tr>
          <td class="header">Constant</td>
          <td class="header">Description</td>
        </tr>
        <tr>
          <td><code>CSS_CM</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in centimeters.
          </td>
        </tr>
        <tr>
          <td><code>CSS_DEG</code></td>
          <td>The value is an {{cssxref("&lt;angle&gt;")}} in degrees.</td>
        </tr>
        <tr>
          <td><code>CSS_DIMENSION</code></td>
          <td>
            The value is a {{cssxref("&lt;number&gt;")}} with an unknown
            dimension.
          </td>
        </tr>
        <tr>
          <td><code>CSS_EMS</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in em units.
          </td>
        </tr>
        <tr>
          <td><code>CSS_EXS</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in ex units.
          </td>
        </tr>
        <tr>
          <td><code>CSS_GRAD</code></td>
          <td>The value is an {{cssxref("&lt;angle&gt;")}} in grads.</td>
        </tr>
        <tr>
          <td><code>CSS_HZ</code></td>
          <td>
            The value is a {{cssxref("&lt;frequency&gt;")}} in Hertz.
            The value can be obtained by using the getFloatValue method.
          </td>
        </tr>
        <tr>
          <td><code>CSS_IN</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in inches.
          </td>
        </tr>
        <tr>
          <td><code>CSS_KHZ</code></td>
          <td>
            The value is a {{cssxref("&lt;frequency&gt;")}} in
            Kilohertz.
          </td>
        </tr>
        <tr>
          <td><code>CSS_MM</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in millimeters.
          </td>
        </tr>
        <tr>
          <td><code>CSS_MS</code></td>
          <td>
            The value is a {{cssxref("&lt;time&gt;")}} in milliseconds.
          </td>
        </tr>
        <tr>
          <td><code>CSS_NUMBER</code></td>
          <td>The value is a simple {{cssxref("&lt;number&gt;")}}.</td>
        </tr>
        <tr>
          <td><code>CSS_PC</code></td>
          <td>The value is a {{cssxref("&lt;length&gt;")}} in picas.</td>
        </tr>
        <tr>
          <td><code>CSS_PERCENTAGE</code></td>
          <td>The value is a {{cssxref("&lt;percentage&gt;")}}.</td>
        </tr>
        <tr>
          <td><code>CSS_PT</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in points.
          </td>
        </tr>
        <tr>
          <td><code>CSS_PX</code></td>
          <td>
            The value is a {{cssxref("&lt;length&gt;")}} in pixels.
          </td>
        </tr>
        <tr>
          <td><code>CSS_RAD</code></td>
          <td>The value is an {{cssxref("&lt;angle&gt;")}} in radians.</td>
        </tr>
        <tr>
          <td><code>CSS_S</code></td>
          <td>The value is a {{cssxref("&lt;time&gt;")}} in seconds.</td>
        </tr>
      </tbody>
    </table>

- floatValue
  - : A `float` representing the new float value.

### Return value

Void.

### Exceptions

| **Type**       | **Description**                                                                                                                                                                                                             |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `DOMException` | An `INVALID_ACCESS_ERR` is raised if the CSS value doesn't contain a float value or if the string value can't be converted into the specified unit. An NO_MODIFICATION_ALLOWED_ERR is raised if this property is read-only. |

## Specifications

This feature was originally defined in the [DOM Style Level 2](https://www.w3.org/TR/DOM-Level-2-Style) specification, but has been dropped from any
standardization effort since then.

It has been superseded by a modern, but incompatible, [CSS Typed Object Model API](/en-US/docs/Web/API/CSS_Typed_OM_API) that is now on the standard track.

## Browser compatibility

{{Compat}}
