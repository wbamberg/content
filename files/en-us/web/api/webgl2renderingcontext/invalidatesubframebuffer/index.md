---
title: WebGL2RenderingContext.invalidateSubFramebuffer()
slug: Web/API/WebGL2RenderingContext/invalidateSubFramebuffer
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGL2
browser-compat: api.WebGL2RenderingContext.invalidateSubFramebuffer
---
{{APIRef("WebGL")}}

The **`WebGL2RenderingContext.invalidateSubFramebuffer()`**
method of the [WebGL 2 API](/en-US/docs/Web/API/WebGL_API) invalidates
portions of the contents of attachments in a framebuffer.

## Syntax

```js
void gl.invalidateSubFramebuffer(target, attachments, x, y, width, height);
```

### Parameters

- `target`

  - : A {{domxref("GLenum")}} specifying the binding point (target). Possible values:

    - `gl.FRAMEBUFFER`: Collection buffer data storage of color, alpha,
      depth and stencil buffers used to render an image.
    - `gl.DRAW_FRAMEBUFFER`: Equivalent to `gl.FRAMEBUFFER`.
    - `gl.READ_FRAMEBUFFER`: Used as a source for reading operations.

- `attachments`

  - : An {{jsxref("Array")}} of {{domxref("GLenum")}} specifying the attachment points to
    invalidate. Possible values:

    - `gl.COLOR_ATTACHMENT{0-15}`: Invalidates one of the framebuffer's
      color buffers.
    - `gl.DEPTH_ATTACHMENT`: Invalidates the framebuffer's depth buffer.
    - `gl.STENCIL_ATTACHMENT`: Invalidates the framebuffer's stencil
      buffer.
    - `gl.DEPTH_STENCIL_ATTACHMENT`: Invalidates both the framebuffer's
      depth and stencil buffer.

- `x`
  - : A {{domxref("GLint")}} specifying the left origin of the pixel rectangle to
    invalidate.
- `y`
  - : A {{domxref("GLint")}} specifying the bottom origin of the pixel rectangle to
    invalidate.
- `width`
  - : A {{domxref("GLsizei")}} specifying the width of the pixel rectangle to invalidate.
- `height`
  - : A {{domxref("GLsizei")}} specifying the height of the pixel rectangle to invalidate.

### Return value

None.

## Examples

```js
gl.invalidateSubFramebuffer(gl.READ_FRAMEBUFFER,
                            [gl.COLOR_ATTACHMENT0, gl.COLOR_ATTACHMENT1],
                            0, 0, 256, 256);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGL2RenderingContext.invalidateFramebuffer()")}}
