---
title: MediaError.code
slug: Web/API/MediaError/code
tags:
  - API
  - Audio
  - Code
  - Errors
  - HTML DOM
  - Media
  - MediaError
  - Property
  - Read-only
  - Reference
  - Video
browser-compat: api.MediaError.code
---
{{APIRef("HTML DOM")}}

The read-only property **`MediaError.code`** returns a numeric
value which represents the kind of error that occurred on a media element. To get a text
string with specific diagnostic information, see {{domxref("MediaError.message")}}.

## Syntax

```js
var myError = mediaError.code;
```

### Value

A numeric value indicating the general type of error which occurred. The possible
values are described below, in {{anch("Media error code constants")}}.

#### Media error code constants

| Name                          | Value | Description                                                                                                                                 |
| ----------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `MEDIA_ERR_ABORTED`           | `1`   | The fetching of the associated resource was aborted by the user's request.                                                                  |
| `MEDIA_ERR_NETWORK`           | `2`   | Some kind of network error occurred which prevented the media from being successfully fetched, despite having previously been available.    |
| `MEDIA_ERR_DECODE`            | `3`   | Despite having previously been determined to be usable, an error occurred while trying to decode the media resource, resulting in an error. |
| `MEDIA_ERR_SRC_NOT_SUPPORTED` | `4`   | The associated resource or media provider object (such as a {{domxref("MediaStream")}}) has been found to be unsuitable.          |

## Example

This example creates a {{HTMLElement("video")}} element, establishes an error handler
for it, and then sets the element's {{htmlattrxref("src", "video")}} attribute to the
video resource to present in the element. The error handler outputs a message

```js
var obj = document.createElement('video');
obj.onerror = function() {console.log("Error with media: " + obj.error.code);}
obj.src="https://example.com/blahblah.mp4";
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The interface defining it, {{domxref("MediaError")}}.
