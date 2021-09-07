---
title: NodeIterator.whatToShow
slug: Web/API/NodeIterator/whatToShow
tags:
  - API
  - DOM
  - NodeIterator
  - Property
browser-compat: api.NodeIterator.whatToShow
---
{{APIRef("DOM")}}

The **`NodeIterator.whatToShow`** read-only property represents
an `unsigned integer` representing a bitmask signifying what types of nodes
should be returned by the {{domxref("NodeIterator")}}.

## Syntax

```js
var nodeTypes = nodeIterator.whatToShow;
```

The values that can be combined to form the bitmask are:

| Constant                                                        | Numerical value                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| --------------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `NodeFilter.SHOW_ALL`                                           | `-1` (that is the max value of `unsigned long`) | Shows all nodes.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `NodeFilter.SHOW_ATTRIBUTE` {{deprecated_inline}}        | `2`                                             | Shows attribute {{ domxref("Attr") }} nodes. This is meaningful only when creating a {{ domxref("NodeIterator") }} or {{ domxref("TreeWalker") }} with an {{ domxref("Attr") }} node as its root; in this case, it means that the attribute node will appear in the first position of the iteration or traversal. Since attributes are never children of other nodes, they do not appear when traversing over the document tree. |
| `NodeFilter.SHOW_CDATA_SECTION` {{deprecated_inline}}    | `8`                                             | Shows {{ domxref("CDATASection") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                              |
| `NodeFilter.SHOW_COMMENT`                                       | `128`                                           | Shows {{ domxref("Comment") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| `NodeFilter.SHOW_DOCUMENT`                                      | `256`                                           | Shows {{ domxref("Document") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| `NodeFilter.SHOW_DOCUMENT_FRAGMENT`                             | `1024`                                          | Shows {{ domxref("DocumentFragment") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                          |
| `NodeFilter.SHOW_DOCUMENT_TYPE`                                 | `512`                                           | Shows {{ domxref("DocumentType") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                              |
| `NodeFilter.SHOW_ELEMENT`                                       | `1`                                             | Shows {{ domxref("Element") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| `NodeFilter.SHOW_ENTITY` {{deprecated_inline}}           | `32`                                            | Legacy, no more used.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `NodeFilter.SHOW_ENTITY_REFERENCE` {{deprecated_inline}} | `16`                                            | Legacy, no more used.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `NodeFilter.SHOW_NOTATION` {{deprecated_inline}}         | `2048`                                          | Legacy, no more used.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `NodeFilter.SHOW_PROCESSING_INSTRUCTION`                        | `64`                                            | Shows {{ domxref("ProcessingInstruction") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                  |
| `NodeFilter.SHOW_TEXT`                                          | `4`                                             | Shows {{ domxref("Text") }} nodes.                                                                                                                                                                                                                                                                                                                                                                                                                          |

## Example

```js
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT + NodeFilter.SHOW_COMMENT + NodeFilter.SHOW_TEXT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
if( (nodeIterator.whatToShow == NodeFilter.SHOW_ALL) ||
    (nodeIterator.whatToShow % (NodeFilter.SHOW_COMMENT*2)) >= NodeFilter.SHOW_COMMENT) {
    // nodeIterator will show comments
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The interface this property belongs to: {{domxref("NodeIterator")}}.
