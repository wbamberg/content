---
title: TextRange
slug: Web/API/TextRange
tags:
  - API
  - DHTML
  - DOM
  - TextRange
---
{{ ApiRef("DOM") }}{{Non-standard_Header}}

> **Warning:** This property is IE specific. Although it is well supported by IE, most other browsers no longer support this property. This property should only be used as one of the solutions when you need to be compatible with lower versions of IE, rather than relying on it completely in cross browser scripts.

A `TextRange` object represents a fragment of text in a document, similar to the standard defined {{domxref("Range")}} interface.

This object is used to represent a specific piece of text in the document. For example, when you hold down the mouse to select the content on the page, you create a typical `TextRange`. It is implemented in IE, then a `TextRange` object can be created by {{domxref("Element.createTextRange()")}} or {{domxref("Document.selection.createRange()")}}.

Note that this interface is not supported in non IE browsers. Alternative {{domxref("Selection")}} and {{domxref("Range")}} interfaces can be used.

## Properties

- {{domxref("TextRange.boundingHeight")}}{{ReadOnlyInline}}
  - : Returns the height of the rectangle bound to the `TextRange` object.
- {{domxref("TextRange.boundingLeft")}}{{ReadOnlyInline}}
  - : Returns the distance between the left edge of the rectangle that binds the `TextRange` object and the left edge that completely contains the `TextRange` object.
- {{domxref("TextRange.boundingTop")}}{{ReadOnlyInline}}
  - : Returns the distance between the top edge of the rectangle that binds the `TextRange` object and the top edge that completely contains the `TextRange` object.
- {{domxref("TextRange.boundingWidth")}}{{ReadOnlyInline}}
  - : Returns the width of the rectangle bound to the `TextRange` object.
- {{domxref("TextRange.htmlText")}}
  - : Gets or sets the HTML content within the `TextRange`.
- {{domxref("TextRange.text")}}
  - : Gets or sets the plaintext content within the `TextRange`.

## Methods

- {{domxref("TextRange.collapse()")}}
  - : Move the caret to the beginning or end of the current range.
- {{domxref("TextRange.duplicate()")}}
  - : Returns a copy of `TextRange`.
- {{domxref("TextRange.execCommand()")}}
  - : Executes a [command](/en-US/docs/Web/API/Document/execCommand) on the current document, the current selection, or the given scope.
- {{domxref("TextRange.expand()")}}
  - : Expand the range to include the full range of specified units. For example, expanding a `"word"` means that the words at both ends of the range will completely included in the range. `xpand to wor` may become `expand to words`, etc.
- {{domxref("TextRange.findText()")}}
  - : Searches the specified text in the original range and adjusts the range to include the first match.
- {{domxref("TextRange.inRange()")}}
  - : Returns whether the current range contains the specified range.
- {{domxref("TextRange.isEqual()")}}
  - : Returns whether the current range is equal to the specified range.
- {{domxref("TextRange.move()")}}
  - : Collapses the range and moves the blank range by a specified number of units. Such as, `move("character",-1)` means to move one character to the left.
- {{domxref("TextRange.moveEnd()")}}
  - : Moves the end of the range by a specified number of units.
- {{domxref("TextRange.moveStart()")}}
  - : Moves the start of the range by a specified number of units.
- {{domxref("TextRange.moveToElementText()")}}
  - : Causes the range to contain the text of the specified element. Can only be used on {{domxref("Element")}} objects.
- {{domxref("TextRange.parentElement()")}}
  - : Returns the parent element of the range, which is the smallest element that contains the range completely. If the selection contains more than one element, when you modify the contents of the selection, the contents will be placed in the corresponding position of the parent element instead of the child element.
- {{domxref("TextRange.pasteHTML()")}}
  - : Paste the HTML content into the given range and replace any previous text and HTML elements in the range.
- {{domxref("TextRange.queryCommandEnabled()")}}
  - : Returns a boolean value indicating whether the specified command can be executed successfully with the `execCommand` method in the current state of the given document. You can also see {{domxref("Document.queryCommandEnabled()")}}.
- {{domxref("TextRange.queryCommandState()")}}
  - : Returns the boolean value indicating the current state of the specified command. You can also see {{domxref("Document.queryCommandState()")}}.
- {{domxref("TextRange.queryCommandValue()")}}
  - : Returns the {{domxref("DOMString")}} indicating the current value of the specified command. You can also see {{domxref("Document.queryCommandValue()")}}.
- {{domxref("TextRange.scrollIntoView()")}}
  - : Scroll the range to the visible range (top or bottom). It can be used as an alternative to {{domxref("Element.scrollIntoView")}} in the lower version of IE.
- {{domxref("TextRange.select()")}}
  - : Select the current range (i.e. the blue selection seen by the user).
- {{domxref("TextRange.setEndPoint()")}}
  - : Sets the end point of the current range based on the bounds of other `TextRange`.

## Example

The following example is valid under IE9. The example gets the `TextRange` through `document.selection`, and sets the specified element to be selected. IE9 supports the standard alternative {{domxref("Range")}}.

```js
var range = document.selection.createRange();
var element = document.getElementById("test");
range.moveToElementText(element);
range.select();
// Selected "SomeTextToBeSelected"
```

```html
<!DOCTYPE html>
<html>
<head>
  <title>TextRange Example</title>
</head>
<body>
  <p id="test">SomeTextToBeSelected</p>
</body>
</html>
```

## Notes

### Use TextRange to Operate the Selection

> **Warning:** Valid only under **IE9**. The {{domxref("selection")}} interface should be used first, if the browser allows it.

{{domxref("document.selection")}} property returns a non-standard `selection` object, and the `selection.createRange()` method creates a `TextRange` object consistent with the currently selection.

```js
var sel = document.selection;
var range = sel.createRange();
alert(range.text);
// Output plaintext of the selection
```

Note that the `createRange` method does not create a reference. If you want to select the modified range after modifying the selection, you need to call the `TextRange.select` method.

### `selection` Compatibility

The `document.selection` object is the primary purpose of `TextRange`. This object is used to process the selected ranges in the document, and is mainly implemented by using the `TextRange` interface. According to the standard, a window / document may have multiple non adjacent selection, but only Firefox can select multiple ranges through <kbd>Ctrl</kbd>; generally, only one selected `TextRange` is allowed in ie.

However, in other browsers, `document` does not have a so-called `selection` attribute - they operate on the selection through the standard [Selection API](/en-US/docs/Web/API/Selection), that is, they get the `Selection` object through the `window.getselection()` method, and use the standard `Range` object to process the text fragment. IE9 and later also gave up the `document.selection` object and switched to the standard interface (although `TextRange` has been reserved, it has lost its function in most cases).

It's easy to get confused. Generally, if the script only needs to be compatible with the latest browser, the standard interface is the best choice; however, the current website still wants to be compatible with IE8 or below browsers. Therefore, the best way is to deal with both at the same time, that is, try to use `TextRange` mode when the standard interface is not supported, but do not regard it as the only choice.

## Browser compatibility

<table class="standard-table">
  <thead>
    <tr>
      <th scope="row"></th>
      <th scope="col">IE</th>
      <th scope="col">Other Browsers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">
        {{domxref("TextRange")}}{{non-standard_inline()}}
      </th>
      <td>≤8(Standard API after IE9)</td>
      <td>
        No Support (See <a href="/en-US/docs/Web/API/Selection">Selection API</a
        >)
      </td>
    </tr>
  </tbody>
</table>

## See also

- {{domxref("Selection")}} and {{domxref("Range")}} standard interface
- [Selection API](/en-US/docs/Web/API/Selection) to replace this non-standard interface
