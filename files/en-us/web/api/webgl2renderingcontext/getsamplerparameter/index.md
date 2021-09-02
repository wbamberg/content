---
title: WebGL2RenderingContext.getSamplerParameter()
slug: Web/API/WebGL2RenderingContext/getSamplerParameter
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGL2
browser-compat: api.WebGL2RenderingContext.getSamplerParameter
---
{{APIRef("WebGL")}}

The **`WebGL2RenderingContext.getSamplerParameter()`** method
of the [WebGL 2 API](/en-US/docs/Web/API/WebGL_API) returns parameter
information of a {{domxref("WebGLSampler")}} object.

## Syntax

```js
any gl.getSamplerParameter(sampler, pname);
```

### Parameters

- sampler
  - : A {{domxref("WebGLSampler")}} object.
- `pname`

  - : A {{domxref("GLenum")}} specifying which information to return. Possible values:

    - `gl.TEXTURE_COMPARE_FUNC`: Returns a {{domxref("GLenum")}} indicating
      the texture comparison function.
    - `gl.TEXTURE_COMPARE_MODE`: Returns a {{domxref("GLenum")}} indicating
      the texture comparison mode.
    - `gl.TEXTURE_MAG_FILTER`: Returns a {{domxref("GLenum")}} indicating
      the texture magnification filter.
    - `gl.TEXTURE_MAX_LOD`: Returns a {{domxref("GLfloat")}} indicating the
      maximum level-of-detail value.
    - `gl.TEXTURE_MIN_FILTER`: Returns a {{domxref("GLenum")}} indicating
      the texture minification filter
    - `gl.TEXTURE_MIN_LOD`: Returns a {{domxref("GLfloat")}} indicating the
      minimum level-of-detail value.
    - `gl.TEXTURE_WRAP_R`: Returns a {{domxref("GLenum")}} indicating the
      texture wrapping function for the texture coordinate r.
    - `gl.TEXTURE_WRAP_S`: Returns a {{domxref("GLenum")}} indicating the
      texture wrapping function for the texture coordinate s.
    - `gl.TEXTURE_WRAP_T`: Returns a {{domxref("GLenum")}} indicating the
      texture wrapping function for the texture coordinate t.

### Return value

Depends on the `pname` parameter, either a {{domxref("GLenum")}} or a
{{domxref("GLfloat")}}.

## Examples

```js
var sampler = gl.createSampler();
gl.getSamplerParameter(sampler, gl.TEXTURE_COMPARE_FUNC);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGLSampler")}}
