---
title: WebGL2RenderingContext.getSyncParameter()
slug: Web/API/WebGL2RenderingContext/getSyncParameter
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGL2
browser-compat: api.WebGL2RenderingContext.getSyncParameter
---
{{APIRef("WebGL")}}

The **`WebGL2RenderingContext.getSyncParameter()`** method of
the [WebGL 2 API](/en-US/docs/Web/API/WebGL_API) returns parameter
information of a {{domxref("WebGLSync")}} object.

## Syntax

```js
any gl.getSyncParameter(sync, pname);
```

### Parameters

- sync
  - : A {{domxref("WebGLSync")}} object.
- `pname`

  - : A {{domxref("GLenum")}} specifying which information to return. Possible values:

    - `gl.OBJECT_TYPE`: Returns a {{domxref("GLenum")}} indicating the type
      of the sync object (always `gl.SYNC_FENCE`).
    - `gl.SYNC_STATUS`: Returns a {{domxref("GLenum")}} indicating the
      status of the sync object (`gl.SIGNALED` or
      `gl.UNSIGNALED`).
    - `gl.SYNC_CONDITION`: Returns a {{domxref("GLenum")}} indicating the
      sync objects' condition (always `gl.SYNC_GPU_COMMANDS_COMPLETE`).
    - `gl.SYNC_FLAGS`: Returns a {{domxref("GLenum")}} indicating the flags
      with which the sync object was created (always 0 as no flags are supported).

### Return value

Depends on the `pname` parameter, either a {{domxref("GLenum")}} or a
{{domxref("GLbitfield")}}.

## Examples

```js
var sync = gl.fenceSync(gl.SYNC_GPU_COMMANDS_COMPLETE, 0);
gl.getSyncParameter(sync, gl.SYNC_STATUS);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGLSync")}}
