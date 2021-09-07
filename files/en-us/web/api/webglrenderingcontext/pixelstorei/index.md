---
title: WebGLRenderingContext.pixelStorei()
slug: Web/API/WebGLRenderingContext/pixelStorei
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGLRenderingContext
browser-compat: api.WebGLRenderingContext.pixelStorei
---
{{APIRef("WebGL")}}

The **`WebGLRenderingContext.pixelStorei()`** method of the [WebGL API](/en-US/docs/Web/API/WebGL_API) specifies the pixel storage modes.

## Syntax

```js
void gl.pixelStorei(pname, param);
```

### Parameters

- pname
  - : A {{domxref("WebGL_API/Types", "GLenum")}} specifying which parameter to set. See below for possible
    values.
- param
  - : A {{domxref("WebGL_API/Types", "GLint")}} specifying a value to set the _`pname`_
    parameter to. See below for possible values.

### Return value

None.

## Pixel storage parameters

| Parameter name (for `pname`)            | Description                                                  | Type                                                     | Default value              | Allowed values (for `param`)          | Specified in  |
| --------------------------------------- | ------------------------------------------------------------ | -------------------------------------------------------- | -------------------------- | ------------------------------------- | ------------- |
| `gl.PACK_ALIGNMENT`                     | Packing of pixel data into memory                            | {{domxref("WebGL_API/Types", "GLint")}}     | 4                          | 1, 2, 4, 8                            | OpenGL ES 2.0 |
| `gl.UNPACK_ALIGNMENT`                   | Unpacking of pixel data from memory.                         | {{domxref("WebGL_API/Types", "GLint")}}     | 4                          | 1, 2, 4, 8                            | OpenGL ES 2.0 |
| `gl.UNPACK_FLIP_Y_WEBGL`                | Flips the source data along its vertical axis if true.       | {{domxref("WebGL_API/Types", "GLboolean")}} | false                      | true, false                           | WebGL         |
| `gl.UNPACK_PREMULTIPLY_ALPHA_WEBGL`     | Multiplies the alpha channel into the other color channels   | {{domxref("WebGL_API/Types", "GLboolean")}} | false                      | true, false                           | WebGL         |
| `gl.UNPACK_COLORSPACE_CONVERSION_WEBGL` | Default color space conversion or no color space conversion. | {{domxref("WebGL_API/Types", "GLenum")}}     | `gl.BROWSER_DEFAULT_WEBGL` | `gl.BROWSER_DEFAULT_WEBGL`, `gl.NONE` | WebGL         |

When using a {{domxref("WebGL2RenderingContext", "WebGL 2 context", "", 1)}}, the
following values are available additionally:

| Constant                 | Description                                                                             | Type                                                 | Default value | Allowed values (for `param`) | Specified in  |
| ------------------------ | --------------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------- | ---------------------------- | ------------- |
| `gl.PACK_ROW_LENGTH`     | Number of pixels in a row.                                                              | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.PACK_SKIP_PIXELS`    | Number of pixel locations skipped before the first pixel is written into memory.        | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.PACK_SKIP_ROWS`      | Number of rows of pixel locations skipped before the first pixel is written into memory | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.UNPACK_ROW_LENGTH`   | Number of pixels in a row.                                                              | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.UNPACK_IMAGE_HEIGHT` | Image height used for reading pixel data from memory                                    | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.UNPACK_SKIP_PIXELS`  | Number of pixel images skipped before the first pixel is read from memory               | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.UNPACK_SKIP_ROWS`    | Number of rows of pixel locations skipped before the first pixel is read from memory    | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |
| `gl.UNPACK_SKIP_IMAGES`  | Number of pixel images skipped before the first pixel is read from memory               | {{domxref("WebGL_API/Types", "GLint")}} | 0             | 0 to `Infinity`              | OpenGL ES 3.0 |

## Examples

Setting the pixel storage mode affects the
{{domxref("WebGLRenderingContext.readPixels()")}} operations, as well as unpacking of
textures with the {{domxref("WebGLRenderingContext.texImage2D()")}} and
{{domxref("WebGLRenderingContext.texSubImage2D()")}} methods.



```js
var tex = gl.createTexture();
gl.bindTexture(gl.TEXTURE_2D, tex);
gl.pixelStorei(gl.PACK_ALIGNMENT, 4);
```

To check the values for packing and unpacking of pixel data, you can query the same
pixel storage parameters with {{domxref("WebGLRenderingContext.getParameter()")}}.

```js
gl.getParameter(gl.PACK_ALIGNMENT);
gl.getParameter(gl.UNPACK_ALIGNMENT);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGLRenderingContext.readPixels()")}}
- {{domxref("WebGLRenderingContext.texImage2D()")}}
- {{domxref("WebGLRenderingContext.texSubImage2D()")}}
