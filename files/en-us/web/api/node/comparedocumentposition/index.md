---
title: Node.compareDocumentPosition()
slug: Web/API/Node/compareDocumentPosition
tags:
  - API
  - Compare Nodes
  - DOM
  - Method
  - Node
  - Position
  - Reference
  - compareDocumentPosition
browser-compat: api.Node.compareDocumentPosition
---
{{APIRef("DOM")}}

The
**`Node.compareDocumentPosition()`** method reports the
position of the given node relative to another node in any document — not just the
given node’s document.

The return value is a [bitmask](<https://en.wikipedia.org/wiki/Mask_(computing)>) of the following
values:

| Name                                        | Value |
| ------------------------------------------- | ----- |
| `DOCUMENT_POSITION_DISCONNECTED`            | 1     |
| `DOCUMENT_POSITION_PRECEDING`               | 2     |
| `DOCUMENT_POSITION_FOLLOWING`               | 4     |
| `DOCUMENT_POSITION_CONTAINS`                | 8     |
| `DOCUMENT_POSITION_CONTAINED_BY`            | 16    |
| `DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC` | 32    |

## Syntax

```js
compareMask = node.compareDocumentPosition(otherNode)
```

### Parameters

- `otherNode`
  - : The other `Node` with which to compare the first
    _`node`_’s document position.

### Return value

An integer value whose bits represent the `otherNode`'s relationship to the
calling `node`.

More than one bit is set if multiple scenarios apply. For example, if
`otherNode` is located earlier in the document **_and_**
contains the `node` on which `compareDocumentPosition()` was
called, then both the `DOCUMENT_POSITION_CONTAINS` and
`DOCUMENT_POSITION_PRECEDING` bits would be set, producing a value of 10
(`0x0A`).

## Example

```js
const head = document.head;
const body = document.body;

if (head.compareDocumentPosition(body) & Node.DOCUMENT_POSITION_FOLLOWING) {
  console.log('Well-formed document');
} else {
  console.error('<head> is not before <body>');
}
```

> **Note:** Because the result returned by
> `compareDocumentPosition()` is a bitmask, the [bitwise AND
> operator](/en-US/docs/JavaScript/Reference/Operators/Bitwise_Operators) must be used for meaningful results.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [`Node.contains()`](/en-US/docs/DOM/Node.contains)
