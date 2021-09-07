---
title: HTMLFontElement.size
slug: Web/API/HTMLFontElement/size
tags:
  - API
  - HTML DOM
  - HTMLFontElement
  - Property
  - Reference
  - Deprecated
browser-compat: api.HTMLFontElement.size
---
{{deprecated_header}}{{ APIRef("HTML DOM") }}

The obsolete
**`HTMLFontElement.size`** property is a
{{domxref("DOMString")}} that reflects the {{ htmlattrxref("size", "font") }} HTML
attribute. It contains either an integer number in the range of 1-7 or a relative
value to increase/decrease the value of the {{htmlattrxref("size", "basefont")}}
attribute of the {{HTMLElement("basefont")}} element.

The format of the string must follow one of the following HTML microsyntaxes:

| Microsyntax              | Description                                                                                                                                                                                                                      | Examples |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| Valid size number string | _integer number in the range of 1-7_                                                                                                                                                                                             | `6`      |
| Relative size string     | _+x or -x, where  x is the number relative to the value of the {{htmlattrxref("size", "basefont")}} attribute of the {{HTMLElement("basefont")}} element_ _(the result should be in the same range of 1-7)_ | `+2 -1`  |

## Syntax

```js
sizeString = fontObj.size;
fontObj.size = sizeString;
```

## Examples

```js
// Assumes there is <font id="f"> element in the HTML

var f = document.getElementById("f");
f.size = "6";
```

## Specifications

The \<font> tag is not supported in HTML5 and as a result neither is
`<font>.size `.

## Browser compatibility

{{Compat}}

## See also

- The {{domxref("HTMLFontElement")}} interface it belongs to.
