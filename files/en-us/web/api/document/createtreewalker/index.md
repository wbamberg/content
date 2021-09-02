---
title: Document.createTreeWalker()
slug: Web/API/Document/createTreeWalker
tags:
  - API
  - DOM
  - DOM Reference
  - Document
  - Method
browser-compat: api.Document.createTreeWalker
---
{{ApiRef("Document")}}

The **`Document.createTreeWalker()`** creator method returns a
newly created {{domxref("TreeWalker")}} object.

## Syntax

```js
document.createTreeWalker(root[, whatToShow[, filter[, expandEntityReferences]]]);
```

### Parameters

- `root`
  - : A root {{domxref("Node")}} of this {{domxref("TreeWalker")}} traversal. Typically
    this will be an element owned by the document.
- `whatToShow` {{optional_inline}}

  - : A `unsigned long` representing a bitmask created by combining the
    constant properties of
    [`NodeFilter`](https://www.w3.org/TR/DOM-Level-2-Traversal-Range/traversal.html#Traversal-NodeFilter).
    It is a convenient way of filtering for certain types of node. It defaults to
    `0xFFFFFFFF` representing the `SHOW_ALL` constant.

    <table class="standard-table">
      <tbody>
        <tr>
          <td class="header">Constant</td>
          <td class="header">Numerical value</td>
          <td class="header">Description</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_ALL</code></td>
          <td>
            <code>-1</code> (that is the max value of <code>unsigned long</code>)
          </td>
          <td>Shows all nodes.</td>
        </tr>
        <tr>
          <td>
            <code>NodeFilter.SHOW_ATTRIBUTE</code> {{deprecated_inline}}
          </td>
          <td><code>2</code></td>
          <td>
            Shows attribute {{domxref("Attr")}} nodes. This is meaningful only
            when creating a {{domxref("TreeWalker")}} with an
            {{domxref("Attr")}} node as its root; in this case, it means that
            the attribute node will appear in the first position of the iteration or
            traversal. Since attributes are never children of other nodes, they do
            not appear when traversing over the document tree.
          </td>
        </tr>
        <tr>
          <td>
            <code>NodeFilter.SHOW_CDATA_SECTION</code> {{deprecated_inline}}
          </td>
          <td><code>8</code></td>
          <td>Shows {{domxref("CDATASection")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_COMMENT</code></td>
          <td><code>128</code></td>
          <td>Shows {{domxref("Comment")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_DOCUMENT</code></td>
          <td><code>256</code></td>
          <td>Shows {{domxref("Document")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_DOCUMENT_FRAGMENT</code></td>
          <td><code>1024</code></td>
          <td>Shows {{domxref("DocumentFragment")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_DOCUMENT_TYPE</code></td>
          <td><code>512</code></td>
          <td>Shows {{domxref("DocumentType")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_ELEMENT</code></td>
          <td><code>1</code></td>
          <td>Shows {{domxref("Element")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_ENTITY</code> {{deprecated_inline}}</td>
          <td><code>32</code></td>
          <td>Legacy, no more usable.</td>
        </tr>
        <tr>
          <td>
            <code>NodeFilter.SHOW_ENTITY_REFERENCE</code>
            {{deprecated_inline}}
          </td>
          <td><code>16</code></td>
          <td>Legacy, no more usable.</td>
        </tr>
        <tr>
          <td>
            <code>NodeFilter.SHOW_NOTATION</code> {{deprecated_inline}}
          </td>
          <td><code>2048</code></td>
          <td>Legacy, no more usable.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_PROCESSING_INSTRUCTION</code></td>
          <td><code>64</code></td>
          <td>Shows {{domxref("ProcessingInstruction")}} nodes.</td>
        </tr>
        <tr>
          <td><code>NodeFilter.SHOW_TEXT</code></td>
          <td><code>4</code></td>
          <td>Shows {{domxref("Text")}} nodes.</td>
        </tr>
      </tbody>
    </table>

- `filter` {{optional_inline}}
  - : A {{domxref("NodeFilter")}}, that is an object with a method
    `acceptNode`, which is called by the {{domxref("TreeWalker")}} to determine
    whether or not to accept a node that has passed the `whatToShow` check.
- `expandEntityReferences` {{optional_inline}} {{deprecated_inline}}
  - : A boolean flag indicating if when discarding an
    entity reference its whole sub-tree must be discarded at the same time.

### Return value

A new {{domxref("TreeWalker")}} object.

## Example

The following example goes through all nodes in the body,
filters out any non nodes that aren't elements (with the \`NodeFilter.SHOW_ELEMENT\` value),
marks each remaining node as acceptable (The `acceptNode()` method could make
a different decision.), and then makes use of tree walker iterator
that is created to advance through the nodes (now all elements) and push them into an
array.

```js
var treeWalker = document.createTreeWalker(
  document.body,
  NodeFilter.SHOW_ELEMENT,
  { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
  false
);

var nodeList = [];
var currentNode = treeWalker.currentNode;

while(currentNode) {
  nodeList.push(currentNode);
  currentNode = treeWalker.nextNode();
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The interface of the object it creates: {{domxref("TreeWalker")}}.
