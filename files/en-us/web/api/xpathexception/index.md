---
title: XPathException
slug: Web/API/XPathException
tags:
  - API
  - DOM
  - DOM XPath API
  - Exception
  - Reference
  - XPath
browser-compat: api.XPathException
---
{{APIRef("DOM XPath")}}{{Deprecated_Header}}

In the [DOM XPath API](/en-US/docs/Web/XPath) the **`XPathException`** interface represents exception conditions that can be encountered while performing XPath operations.

## Properties

- {{domxref("XPathException.code")}} {{readOnlyInline}}
  - : Returns a `short` that contains one of the {{anch("Error codes", "error code constants")}}.

## Constants

| Constant                 | Value | Description                                                                                                                                                                                                                                                |
| ------------------------ | ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `INVALID_EXPRESSION_ERR` | `51`  | If the expression has a syntax error or otherwise is not a legal expression according to the rules of the specific {{domxref("XPathEvaluator")}} or contains specialized extension functions or variables not supported by this implementation. |
| `TYPE_ERR`               | `52`  | If the expression cannot be converted to return the specified type.                                                                                                                                                                                        |

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{DOMxRef("Document.createExpression()")}}
- {{DOMxRef("XPathExpression")}}
