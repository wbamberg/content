---
title: XPathResult.resultType
slug: Web/API/XPathResult/resultType
tags:
  - API
  - DOM XPath API
  - Property
  - Reference
  - XPath
  - XPathResult
browser-compat: api.XPathResult.resultType
---
{{APIRef("DOM XPath")}}

The read-only **`resultType`** property of the
{{domxref("XPathResult")}} interface represents the type of the result, as defined by
the type constants.

{{AvailableInWorkers}}

## Syntax

```js
var resultType = result.resultType;
```

### Return value

An integer value representing the type of the result, as defined by the [type constants](#).

## Constants

| Result Type Defined Constant   | Value | Description                                                                                                                                                                                        |
| ------------------------------ | ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ANY_TYPE`                     | `0`   | A result set containing whatever type naturally results from evaluation of the expression. Note that if the result is a node-set then `UNORDERED_NODE_ITERATOR_TYPE` is always the resulting type. |
| `NUMBER_TYPE`                  | `1`   | A result containing a single number. This is useful for example, in an XPath expression using the `count()` function.                                                                              |
| `STRING_TYPE`                  | `2`   | A result containing a single string.                                                                                                                                                               |
| `BOOLEAN_TYPE`                 | `3`   | A result containing a single boolean value. This is useful for example, in an XPath expression using the `not()` function.                                                                         |
| `UNORDERED_NODE_ITERATOR_TYPE` | `4`   | A result node-set containing all the nodes matching the expression. The nodes may not necessarily be in the same order that they appear in the document.                                           |
| `ORDERED_NODE_ITERATOR_TYPE`   | `5`   | A result node-set containing all the nodes matching the expression. The nodes in the result set are in the same order that they appear in the document.                                            |
| `UNORDERED_NODE_SNAPSHOT_TYPE` | `6`   | A result node-set containing snapshots of all the nodes matching the expression. The nodes may not necessarily be in the same order that they appear in the document.                              |
| `ORDERED_NODE_SNAPSHOT_TYPE`   | `7`   | A result node-set containing snapshots of all the nodes matching the expression. The nodes in the result set are in the same order that they appear in the document.                               |
| `ANY_UNORDERED_NODE_TYPE`      | `8`   | A result node-set containing any single node that matches the expression. The node is not necessarily the first node in the document that matches the expression.                                  |
| `FIRST_ORDERED_NODE_TYPE`      | `9`   | A result node-set containing the first node in the document that matches the expression.                                                                                                           |

## Example

The following example shows the use of the `resultType` property.

### HTML

```html
<div>XPath example</div>
<div>Is XPath result a node set: <output></output></div>
```

### JavaScript

```js
var xpath = "//div";
var result = document.evaluate(xpath, document, null, XPathResult.ANY_TYPE, null);
document.querySelector("output").textContent =
  result.resultType >= XPathResult.UNORDERED_NODE_ITERATOR_TYPE &&
  result.resultType <= XPathResult.FIRST_ORDERED_NODE_TYPE;
```

### Result

{{EmbedLiveSample('Example', 400, 70)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
