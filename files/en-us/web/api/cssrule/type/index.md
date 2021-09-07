---
title: CSSRule.type
slug: Web/API/CSSRule/type
tags:
  - API
  - CSSOM
  - Property
  - Reference
  - Read-only
  - Deprecated
browser-compat: api.CSSRule.type
---
{{APIRef("CSSOM")}}{{Deprecated_header}}

The read-only **`type`** property of the
{{domxref("CSSRule")}} interface is a deprecated property that returns an integer
indicating which type of rule the {{domxref("CSSRule")}} represents.

## Syntax

```js
var type = cssRule.type;
```

### Value

An integer which will be one of the type constants listed in the table below.

| Type                               | Value | Rule-specific interface                                                       | Comments and examples                                                                                                                                                                                                                                     |
| ---------------------------------- | ----- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `CSSRule.STYLE_RULE`               | `1`   | {{domxref("CSSStyleRule")}}                                          | The most common kind of rule: `selector { prop1: val1; prop2: val2; }`                                                                                                                                                                                    |
| `CSSRule.IMPORT_RULE`              | `3`   | {{domxref("CSSImportRule")}}                                          | An {{cssxref("@import")}} rule. (Until the documentation is completed, see the interface definition in the Mozilla source code: [nsIDOMCSSImportRule](http://mxr.mozilla.org/mozilla-central/source/dom/interfaces/css/nsIDOMCSSImportRule.idl#9).) |
| `CSSRule.MEDIA_RULE`               | `4`   | {{domxref("CSSMediaRule")}}                                          |                                                                                                                                                                                                                                                           |
| `CSSRule.FONT_FACE_RULE`           | `5`   | {{domxref("CSSFontFaceRule")}}                                      |                                                                                                                                                                                                                                                           |
| `CSSRule.PAGE_RULE`                | `6`   | {{domxref("CSSPageRule")}}                                          |                                                                                                                                                                                                                                                           |
| `CSSRule.KEYFRAMES_RULE`           | `7`   | {{domxref("CSSKeyframesRule")}} {{experimental_inline}}     |                                                                                                                                                                                                                                                           |
| `CSSRule.KEYFRAME_RULE`            | `8`   | {{domxref("CSSKeyframeRule")}} {{experimental_inline}}     |                                                                                                                                                                                                                                                           |
| _Reserved for future use_          | `9`   |                                                                               | Should be used to define color profiles in the future                                                                                                                                                                                                     |
| `CSSRule.NAMESPACE_RULE`           | `10`  | {{domxref("CSSNamespaceRule")}} {{experimental_inline}}     |                                                                                                                                                                                                                                                           |
| `CSSRule.COUNTER_STYLE_RULE`       | `11`  | {{domxref("CSSCounterStyleRule")}} {{experimental_inline}} |                                                                                                                                                                                                                                                           |
| `CSSRule.SUPPORTS_RULE`            | `12`  | {{domxref("CSSSupportsRule")}}                                      |                                                                                                                                                                                                                                                           |
| `CSSRule.DOCUMENT_RULE`            | `13`  | {{domxref("CSSDocumentRule")}} {{experimental_inline}}     |                                                                                                                                                                                                                                                           |
| `CSSRule.FONT_FEATURE_VALUES_RULE` | `14`  | {{domxref("CSSFontFeatureValuesRule")}}                          |                                                                                                                                                                                                                                                           |
| `CSSRule.VIEWPORT_RULE`            | `15`  | {{domxref("CSSViewportRule")}} {{experimental_inline}}     |                                                                                                                                                                                                                                                           |
| `CSSRule.REGION_STYLE_RULE`        | `16`  | {{domxref("CSSRegionStyleRule")}} {{experimental_inline}} |                                                                                                                                                                                                                                                           |
| `CSSRule.UNKNOWN_RULE`             | `0`   | {{domxref("CSSUnknownRule")}} {{deprecated_inline}}         |                                                                                                                                                                                                                                                           |
| `CSSRule.CHARSET_RULE`             | `2`   | `CSSCharsetRule` {{deprecated_inline}}                                 | (Removed in most browsers.)                                                                                                                                                                                                                               |

## Examples

```js
let myRules = document.styleSheets[0].cssRules;
console.log(myRules[0].type);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
