---
title: CSSPrimitiveValue.primitiveType
slug: Web/API/CSSPrimitiveValue/primitiveType
tags:
  - API
  - CSSPrimitiveValue
  - Property
  - Read-only
  - Reference
  - primitiveValue
browser-compat: api.CSSPrimitiveValue.primitiveType
---
{{APIRef("CSSOM")}}

The **`primitiveType`** read-only property of the
{{domxref("CSSPrimitiveValue")}} interface represents the type of a CSS value.

> **Note:** This property was part of an attempt to create a typed CSS Object Model. This attempt has been abandoned, and most browsers do
> not implement it.
>
> To achieve your purpose, you can use:
>
> - the untyped [CSS Object Model](/en-US/docs/Web/API/CSS_Object_Model), widely supported, or
> - the modern [CSS Typed Object Model API](/en-US/docs/Web/API/CSS_Typed_OM_API), less supported and considered experimental.

## Syntax

```js
type = cssPrimitiveValue.primitiveType;
```

### Value

An `unsigned short` representing the type of the value. Possible values are:

| Constant         | Description                                                                                                                                                                      |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `CSS_ATTR`       | The value is an {{cssxref("attr()")}} function. The value can be obtained by using the `getStringValue()` method.                                                         |
| `CSS_CM`         | The value is a {{cssxref("&lt;length&gt;")}} in centimeters. The value can be obtained by using the `getFloatValue()` method.                                         |
| `CSS_COUNTER`    | The value is a [counter or counters](/en-US/docs/Web/CSS/CSS_Lists_and_Counters/Using_CSS_counters) function. The value can be obtained by using the `getCounterValue()` method. |
| `CSS_DEG`        | The value is an {{cssxref("&lt;angle&gt;")}} in degrees. The value can be obtained by using the `getFloatValue()` method.                                                |
| `CSS_DIMENSION`  | The value is a {{cssxref("&lt;number&gt;")}} with an unknown dimension. The value can be obtained by using the `getFloatValue()` method.                              |
| `CSS_EMS`        | The value is a {{cssxref("&lt;length&gt;")}} in em units. The value can be obtained by using the `getFloatValue()` method.                                            |
| `CSS_EXS`        | The value is a {{cssxref("&lt;length&gt;")}} in ex units. The value can be obtained by using the `getFloatValue()` method.                                            |
| `CSS_GRAD`       | The value is an {{cssxref("&lt;angle&gt;")}} in grads. The value can be obtained by using the `getFloatValue()` method.                                                  |
| `CSS_HZ`         | The value is a {{cssxref("&lt;frequency&gt;")}} in Hertz. The value can be obtained by using the getFloatValue method.                                               |
| `CSS_IDENT`      | The value is an identifier. The value can be obtained by using the `getStringValue()` method.                                                                                    |
| `CSS_IN`         | The value is a {{cssxref("&lt;length&gt;")}} in inches. The value can be obtained by using the `getFloatValue()` method.                                              |
| `CSS_KHZ`        | The value is a {{cssxref("&lt;frequency&gt;")}} in Kilohertz. The value can be obtained by using the `getFloatValue()` method.                                       |
| `CSS_MM`         | The value is a {{cssxref("&lt;length&gt;")}} in millimeters. The value can be obtained by using the `getFloatValue()` method.                                         |
| `CSS_MS`         | The value is a {{cssxref("&lt;time&gt;")}} in milliseconds. The value can be obtained by using the `getFloatValue()` method.                                            |
| `CSS_NUMBER`     | The value is a simple {{cssxref("&lt;number&gt;")}}. The value can be obtained by using the `getFloatValue()` method.                                                 |
| `CSS_PC`         | The value is a {{cssxref("&lt;length&gt;")}} in picas. The value can be obtained by using the `getFloatValue()` method.                                               |
| `CSS_PERCENTAGE` | The value is a {{cssxref("&lt;percentage&gt;")}}. The value can be obtained by using the `getFloatValue()` method.                                                    |
| `CSS_PT`         | The value is a {{cssxref("&lt;length&gt;")}} in points. The value can be obtained by using the `getFloatValue()` method.                                              |
| `CSS_PX`         | The value is a {{cssxref("&lt;length&gt;")}} in pixels. The value can be obtained by using the `getFloatValue()` method.                                              |
| `CSS_RAD`        | The value is an {{cssxref("&lt;angle&gt;")}} in radians. The value can be obtained by using the `getFloatValue()` method.                                                |
| `CSS_RECT`       | The value is a {{cssxref("shape", "rect()", "#Syntax")}} function. The value can be obtained by using the `getRectValue()` method.                                |
| `CSS_RGBCOLOR`   | The value is an {{cssxref("&lt;color&gt;")}}. The value can be obtained by using the `getRGBColorValue()` method.                                                        |
| `CSS_S`          | The value is a {{cssxref("&lt;time&gt;")}} in seconds. The value can be obtained by using the `getFloatValue()` method.                                                 |
| `CSS_STRING`     | The value is a {{cssxref("&lt;string&gt;")}}. The value can be obtained by using the `getStringValue()` method.                                                       |
| `CSS_UNKNOWN`    | The value is not a recognized CSS2 value. The value can only be obtained by using the {{domxref("CSSValue.cssText", "cssText")}} attribute.                        |
| `CSS_URI`        | The value is a {{cssxref("url()")}}. The value can be obtained by using the `getStringValue()` method.                                                                   |

## Example

```js
var cs = window.getComputedStyle(document.body);
var cssValue = cs.getPropertyCSSValue("color");
console.log(cssValue.primitiveType);
```

## Specifications

This feature was originally defined in the [DOM Style Level 2](https://www.w3.org/TR/DOM-Level-2-Style) specification, but has been dropped from any
standardization effort since then.

It has been superseded by a modern, but incompatible, [CSS Typed Object Model API](/en-US/docs/Web/API/CSS_Typed_OM_API) that is now on the standard track.

## Browser compatibility

{{Compat}}

## See also

- {{domxref("CSSStyleDeclaration.getPropertyCSSValue()")}}
