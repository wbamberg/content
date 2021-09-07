---
title: FileReader.result
slug: Web/API/FileReader/result
tags:
  - API
  - File API
  - FileReader
  - Files
  - Property
  - Reference
  - result
browser-compat: api.FileReader.result
---
{{APIRef("File API")}}

The {{domxref("FileReader")}} **`result`** property returns the
file's contents. This property is only valid after the read operation is complete, and
the format of the data depends on which of the methods was used to initiate the read
operation.

## Syntax

```js
var file = instanceOfFileReader.result
```

### Value

An appropriate string or {{jsxref("ArrayBuffer")}} based on which of the reading methods
was used to initiate the read operation. The value is `null` if the reading
is not yet complete or was unsuccessful.

The result types are described below.

| Method                                                                                       | Description                                                                                                                               |
| -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| {{domxref("FileReader/readAsArrayBuffer", "readAsArrayBuffer()")}}     | The `result` is a JavaScript {{jsxref("Global_Objects/ArrayBuffer",
        "ArrayBuffer")}} containing binary data. |
| {{domxref("FileReader/readAsBinaryString", "readAsBinaryString()")}} | The `result` contains the raw binary data from the file in a string.                                                                      |
| {{domxref("FileReader/readAsDataURL", "readAsDataURL()")}}                 | The `result` is a string with a `data:` URL representing the file's data.                                                                 |
| {{domxref("FileReader/readAsText", "readAsText()")}}                         | The `result` is text in a string.                                                                                                         |

## Example

This example presents a function, `read()`, which reads a file from a [file input](/en-US/docs/Web/HTML/Element/input/file). It works by creating a
{{domxref("FileReader")}} object and creating a listener for
{{domxref("FileReader/load_event", "load")}} events such that when then file is read,
the `result` is obtained and passed to the callback function provided to
`read()`.

The content is handled as raw text data.

```js
var fileInput = document.querySelector('input[type="file"]');

function read(callback) {
  var file = fileInput.files.item(0);
  var reader = new FileReader();

  reader.onload = function() {
    callback(reader.result);
  }

  reader.readAsText(file);
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("FileReader")}}
