---
title: Window.showModalDialog()
slug: Web/API/Window/showModalDialog
tags:
  - API
  - Deprecated
  - HTML DOM
  - Method
  - Window
browser-compat: api.Window.showModalDialog
---
{{deprecated_header}}{{APIRef}}

> **Warning:** This feature has been removed. Please fix your Web sites and applications.
>
> This method was removed in Chrome 43 and Firefox 56.

The **`Window.showModalDialog()`**
created and displayed a modal dialog box containing a specified HTML document.

## Syntax

```js
returnVal = window.showModalDialog(uri[, arguments][, options]);
```

- `returnVal` holds the `returnValue` property as set by the
  document specified by `uri`.
- `uri` is the URL of the document to display in the dialog.
- `arguments` is an optional variant containing values passed to the
  dialog; these are made available in the
  [`window`](/en-US/docs/Web/API/Window) object's
  [`window.dialogArguments`](/en-US/docs/Web/API/Window/dialogArguments)
  property.
- `options` is an optional string specifying window ornamentation for the
  dialog, using one or more semicolon delimited values:

| Syntax                                           | Description                                                                                                                                          |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `center: {on \| off \| yes \| no \| 1 \| 0 }`    | If `on`, `yes`, or `1`, the dialog window is centered on the desktop; otherwise it's hidden. Default is `yes`.                                       |
| `dialogheight: height`                           | The height of the dialog box in pixels.                                                                                                              |
| `dialogleft: left`                               | Distance of the dialog box from the left edge of the desktop.                                                                                        |
| `dialogwidth: width`                             | The width of the dialog box in pixels.                                                                                                               |
| `dialogtop: top`                                 | Distance of the dialog box from the top edge of the desktop.                                                                                         |
| `resizable: {on \| off \| yes \| no \| 1 \| 0 }` | If this argument's value is `on`, `yes`, or 1, the dialog window can be resized by the user; otherwise its size is fixed. The default value is `no`. |
| `scroll: {on \| off \| yes \| no \| 1 \| 0 }`    | If `on`, `yes`, or 1, the dialog window has scroll bars; otherwise its size is fixed. Default is `no`.                                               |

> **Note:** Firefox does not implement the `dialogHide`, `edge`, `status`, or `unadorned` arguments.

## Notes

`showModalDialog()` was briefly standardized as part of HTML5. The third
argument for additional options was not present in the HTML5 version.

## Specifications

- [MSDN page
  for `showModalDialog`](<https://msdn.microsoft.com/en-us/library/ms536759(VS.85).aspx>)

## Browser compatibility

{{Compat}}

## See also

- {{HTMLElement("dialog")}}, a replacement for `window.showModalDialog()`.
- [showModalDialog Polyfill](https://github.com/niutech/showModalDialog)
  using a {{HTMLElement("dialog")}} and [generators](/en-US/docs/Web/JavaScript/Reference/Statements/function*)
