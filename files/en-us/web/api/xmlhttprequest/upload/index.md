---
title: XMLHttpRequest.upload
slug: Web/API/XMLHttpRequest/upload
tags:
  - AJAX
  - API
  - Monitoring XMLHttpRequest
  - Property
  - Read-only
  - Reference
  - Sending Files
  - Uploading
  - XHR
  - XHR Uploads
  - XMLHttpRequest
  - XMLHttpRequest Uploads
  - XMLHttpRequestUpload
  - upload
browser-compat: api.XMLHttpRequest.upload
---
{{APIRef('XMLHttpRequest')}}

The {{domxref("XMLHttpRequest")}} `upload` property returns an {{domxref("XMLHttpRequestUpload")}} object that can be observed to monitor an upload's progress.

It is an opaque object, but because it's also an {{domxref("XMLHttpRequestEventTarget")}}, event listeners can be attached to track its process.

> **Note:** Attaching event listeners to this object prevents the request from being a "simple request" and will cause a preflight request to be issued if cross-origin; see [CORS](/en-US/docs/Web/HTTP/CORS). Because of this, event listeners need to be registered before calling {{domxref("XMLHttpRequest.send", "send()")}} or upload events won't be dispatched.

> **Note:** The spec also seems to indicate that event listeners should be attached after {{domxref("XMLHttpRequest.open", "open()")}}. However, browsers are buggy on this matter, and often need the listeners to be registered _before_ {{domxref("XMLHttpRequest.open", "open()")}} to work.

The following events can be triggered on an upload object and used to monitor the upload:

| Event                        | Event listener                                                               | Description                                                                                                                                                                                                                                                                              |
| ---------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| {{event("loadstart")}} | {{domxref("XMLHttpRequest.onloadstart", "onloadstart")}} | The upload has begun.                                                                                                                                                                                                                                                                    |
| {{event("progress")}} | {{domxref("XMLHttpRequest.onprogress", "onprogress")}}     | Periodically delivered to indicate the amount of progress made so far.                                                                                                                                                                                                                   |
| {{event("abort")}}     | {{domxref("XMLHttpRequest.onabort", "onabort")}}             | The upload operation was aborted.                                                                                                                                                                                                                                                        |
| {{event("error")}}     | {{domxref("XMLHttpRequest.onerror", "onerror")}}             | The upload failed due to an error.                                                                                                                                                                                                                                                       |
| {{event("load")}}     | {{domxref("XMLHttpRequest.onload", "onload")}}                 | The upload completed successfully.                                                                                                                                                                                                                                                       |
| {{event("timeout")}} | {{domxref("XMLHttpRequest.ontimeout", "ontimeout")}}         | The upload timed out because a reply did not arrive within the time interval specified by the {{domxref("XMLHttpRequest.timeout")}}.                                                                                                                                          |
| {{event("loadend")}} | {{domxref("XMLHttpRequest.onloadend", "onloadend")}}         | The upload finished. This event does not differentiate between success or failure, and is sent at the end of the upload regardless of the outcome. Prior to this event, one of `load`, `error`, `abort`, or `timeout` will already have been delivered to indicate why the upload ended. |

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using XMLHttpRequest](/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)
- [FileHandle API](/en-US/docs/Web/API/File_Handle_API)
- [File and Directory Entries API](/en-US/docs/Web/API/File_and_Directory_Entries_API)
