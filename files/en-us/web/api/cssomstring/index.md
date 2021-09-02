---
title: CSSOMString
slug: Web/API/CSSOMString
tags:
  - API
  - CSSOM
  - Reference
---
{{APIRef("DOM")}}

**`CSSOMString`** is used to denote string data in [CSSOM](/en-US/docs/Web/API/CSS_Object_Model) specifications and can refer to either {{domxref("DOMString")}} or {{domxref("USVString")}}. When a specification says `CSSOMString`, it depends on the browser vendors to choose whether to use `DOMString` or `USVString`. While browser implementations that use UTF-8 internally to represent strings in memory can use `USVString` when the specification says `CSSOMString`, implementations that already represent strings as 16-bit sequences might choose to use `DOMString` instead.

#### Implementation differences

<table class="standard-table">
  <tbody>
    <tr>
      <td class="header">Browser</td>
      <td class="header">DOMString or USVString for CSSOMString</td>
    </tr>
    <tr>
      <td>Firefox (Gecko)</td>
      <td>USVString</td>
    </tr>
    <tr>
      <td>Chrome (Blink)</td>
      <td>USVString</td>
    </tr>
    <tr>
      <td>Safari (WebKit)</td>
      <td>USVString</td>
    </tr>
    <tr>
      <td>Edge (EdgeHTML)</td>
      <td>-</td>
    </tr>
    <tr>
      <td>Opera (Blink)</td>
      <td>USVString</td>
    </tr>
  </tbody>
</table>

## Specifications

| Specification                                                                | Status                   | Comment             |
| ---------------------------------------------------------------------------- | ------------------------ | ------------------- |
| {{SpecName('CSSOM', '#cssomstring-type', 'CSSOMString')}} | {{Spec2("CSSOM")}} | Initial definition. |

## See also

- {{jsxref("Global_Objects/String", "String")}}
- {{domxref("CSS_Object_Model")}}
- {{domxref("DOMString")}}
- {{domxref("USVString")}}
- [Binary strings](/en-US/docs/Web/API/DOMString/Binary)
