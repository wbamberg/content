---
title: Document.rootElement
slug: Web/API/Document/rootElement
tags:
  - API
  - DOM
  - Deprecated
  - Document
  - Property
  - Reference
  - SVG
  - root
---
{{ApiRef("DOM")}}{{Deprecated_header}}

**`Document.rootElement`** returns the {{domxref("Element")}}
that is the root element of the {{domxref("document")}} if it is an
{{SVGElement("svg")}} element, otherwise `null`. It is deprecated in favor of
{{domxref("Document.documentElement")}}, which returns the root element for all
documents.

## Syntax

```js
const element = document.rootElement
```

## Notes

If the document is a non-empty SVG document, then the `rootElement` will be
an {{domxref("SVGSVGElement")}}, identical to the `documentElement`.

## Specifications

| Specification                                                                                                                | Status                   | Comment            |
| ---------------------------------------------------------------------------------------------------------------------------- | ------------------------ | ------------------ |
| {{SpecName('SVG2','struct.html#__svg__SVGDocument__rootElement','SVGDocument.rootElement')}} | {{Spec2('SVG2')}} | Deprecated         |
| {{SpecName('SVG1.1','struct.html#__svg__SVGDocument__rootElement','SVGDocument.rootElement')}} | {{Spec2('SVG1.1')}} | Initial definition |
