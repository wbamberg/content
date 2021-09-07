---
title: Document.queryCommandState()
slug: Web/API/Document/queryCommandState
tags:
  - API
  - DOM
  - Reference
  - Deprecated
browser-compat: api.Document.queryCommandState
---
{{ApiRef("DOM")}}{{deprecated_header}}

The **`queryCommandState()`** method will tell you if the current selection has a certain {{domxref("Document.execCommand()")}} command applied.

## Syntax

```js
queryCommandState(String command)
```

### Parameters

`command` is a command from {{domxref("Document.execCommand()")}}

### Return value

`queryCommandState()` can return a boolean value or `null` if the state is unknown.

## Example

### HTML

```html
<div contenteditable="true">Select a part of this text!</div>
<button onclick="makeBold();">Test the state of the 'bold' command</button>
```

### JavaScript

```js
function makeBold() {
  var state = document.queryCommandState("bold");
  switch (state) {
    case true:
      alert("The bold formatting will be removed from the selected text.");
      break;
    case false:
      alert("The selected text will be displayed in bold.");
      break;
    case null:
      alert("The state of the 'bold' command is indeterminable.");
      break;
  }
  document.execCommand('bold');
}
```

### Result

{{EmbedLiveSample('Example')}}

## Specifications

This feature is not part of any current specification. It is no longer on track to become a standard.

## Browser compatibility

{{Compat}}

## See also

- {{domxref("HTMLElement.contentEditable")}}
- {{domxref("document.designMode")}}
- [Rich-Text Editing in Mozilla](/en-US/docs/Web/Guide/HTML/Editable_content/Rich-Text_Editing_in_Mozilla)
- Browser bugs related to `queryCommandState()`: [Scribe's "Browser Inconsistencies" documentation](https://github.com/guardian/scribe/blob/master/BROWSERINCONSISTENCIES.md#documentquerycommandstate)
