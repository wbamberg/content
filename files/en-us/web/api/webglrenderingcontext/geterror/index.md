---
title: WebGLRenderingContext.getError()
slug: Web/API/WebGLRenderingContext/getError
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGLRenderingContext
browser-compat: api.WebGLRenderingContext.getError
---
{{APIRef("WebGL")}}

The **`WebGLRenderingContext.getError()`** method of the [WebGL API](/en-US/docs/Web/API/WebGL_API) returns error information.

## Syntax

```js
GLenum gl.getError();
```

### Parameters

None.

### Return value

| Constant                           | Description                                                                                                                                                         |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `gl.NO_ERROR`                      | No error has been recorded. The value of this constant is 0.                                                                                                        |
| `gl.INVALID_ENUM`                  | An unacceptable value has been specified for an enumerated argument. The command is ignored and the error flag is set.                                              |
| `gl.INVALID_VALUE`                 | A numeric argument is out of range. The command is ignored and the error flag is set.                                                                               |
| `gl.INVALID_OPERATION`             | The specified command is not allowed for the current state. The command is ignored and the error flag is set.                                                       |
| `gl.INVALID_FRAMEBUFFER_OPERATION` | The currently bound framebuffer is not framebuffer complete when trying to render to or to read from it.                                                            |
| `gl.OUT_OF_MEMORY`                 | Not enough memory is left to execute the command.                                                                                                                   |
| `gl.CONTEXT_LOST_WEBGL`            | If the WebGL context is lost, this error is returned on the first call to `getError`. Afterwards and until the context has been restored, it returns `gl.NO_ERROR`. |

## Examples

```js
gl.getError(); // gl.NO_ERROR (0)

gl.enable(gl.FOOBAR);
gl.getError(); // gl.INVALID_ENUM;
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGLRenderingContext")}}
- {{domxref("WebGLContextEvent")}}
