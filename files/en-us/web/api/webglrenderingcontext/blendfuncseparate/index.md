---
title: WebGLRenderingContext.blendFuncSeparate()
slug: Web/API/WebGLRenderingContext/blendFuncSeparate
tags:
  - API
  - Method
  - Reference
  - WebGL
  - WebGLRenderingContext
browser-compat: api.WebGLRenderingContext.blendFuncSeparate
---
{{APIRef("WebGL")}}

The **`WebGLRenderingContext.blendFuncSeparate()`** method of
the [WebGL API](/en-US/docs/Web/API/WebGL_API) defines which function is used
for blending pixel arithmetic for RGB and alpha components separately.

## Syntax

```js
void gl.blendFuncSeparate(srcRGB, dstRGB, srcAlpha, dstAlpha);
```

### Parameters

- `srcRGB`
  - : A {{domxref("WebGL_API.Types")}} specifying a multiplier for the red, green and blue (RGB)
    source blending factors. The default value is `gl.ONE`. For possible
    values, see below.
- `dstRGB`
  - : A {{domxref("WebGL_API.Types")}} specifying a multiplier for the red, green and blue (RGB)
    destination blending factors. The default value is `gl.ZERO`. For possible
    values, see below.
- `srcAlpha`
  - : A {{domxref("WebGL_API.Types")}} specifying a multiplier for the alpha source blending
    factor. The default value is `gl.ONE`. For possible values, see below.
- `dstAlpha`
  - : A {{domxref("WebGL_API.Types")}} specifying a multiplier for the alpha destination blending
    factor. The default value is `gl.ZERO`. For possible values, see below.

### Return value

None.

### Exceptions

- If _srcRGB_, _dstRGB_, _srcAlpha_, or _dstAlpha_ is not
  one of the listed possible values, a `gl.INVALID_ENUM` error is thrown.
- If a constant color and a constant alpha value are used together as source
  (`srcRGB`) and destination (`dstRGB`) factors, a
  `gl.INVALID_ENUM` error is thrown.

## Constants

The following constants can be used for _srcRGB_, _dstRGB_,
_srcAlpha_, and _dstAlpha_

The formulas for the blending factors can be described like this (all RGBA values are
between 0 and 1):

- color(RGB) = (sourceColor \* _srcRGB_) + (destinationColor \* _dstRGB_)
- color(A) = (sourceAlpha \* _srcAlpha_) + (destinationAlpha \*
  _dstAlpha_)

In the following table, R<sub>S</sub>, G<sub>S</sub>, B<sub>S</sub>, A<sub>S</sub> represent respectively
the _red_, _green_, _blue_ and _alpha_ component of the source, while
R<sub>D</sub>, G<sub>D</sub>, B<sub>D</sub>, A<sub>D</sub> represent respectively
the _red_, _green_, _blue_ and _alpha_ component of the destination.
Similarly, R<sub>C</sub>, G<sub>C</sub>, B<sub>C</sub>, A<sub>C</sub> represent respectively
the _red_, _green_, _blue_ and _alpha_ component of a constant color.
They are all values between 0 and 1, included.

| Constant                      | RGB factor                                                                                                          | Alpha factor    | Description                                                                                                                                                        |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `gl.ZERO`                     | 0,0,0                                                                                                               | 0               | Multiplies all colors by 0.                                                                                                                                        |
| `gl.ONE`                      | 1,1,1,1                                                                                                             | 1               | Multiplies all colors by 1.                                                                                                                                        |
| `gl.SRC_COLOR`                | R<sub>S</sub>, G<sub>S</sub>, B<sub>S</sub>                                                                         | A<sub>S</sub>   | Multiplies all colors by the source colors.                                                                                                                        |
| `gl.ONE_MINUS_SRC_COLOR`      | 1-R<sub>S</sub>, 1-G<sub>S</sub>, 1-B<sub>S</sub>                                                                   | 1-A<sub>S</sub> | Multiplies all colors by 1 minus each source color.                                                                                                                |
| `gl.DST_COLOR`                | R<sub>D</sub>, G<sub>D</sub>, B<sub>D</sub>                                                                         | A<sub>D</sub>   | Multiplies all colors by the destination color.                                                                                                                    |
| `gl.ONE_MINUS_DST_COLOR`      | 1-R<sub>D</sub>, 1-G<sub>D</sub>, 1-B<sub>D</sub>                                                                   | 1-A<sub>D</sub> | Multiplies all colors by 1 minus each destination color.                                                                                                           |
| `gl.SRC_ALPHA`                | A<sub>S</sub>, A<sub>S</sub>, A<sub>S</sub>                                                                         | A<sub>S</sub>   | Multiplies all colors by the source alpha color.                                                                                                                   |
| `gl.ONE_MINUS_SRC_ALPHA`      | 1-A<sub>S</sub>, 1-A<sub>S</sub>, 1-A<sub>S</sub>                                                                   | 1-A<sub>S</sub> | Multiplies all colors by 1 minus the source alpha color.                                                                                                           |
| `gl.DST_ALPHA`                | A<sub>D</sub>, A<sub>D</sub>, A<sub>D</sub>                                                                         | A<sub>D</sub>   | Multiplies all colors by the destination alpha color.                                                                                                              |
| `gl.ONE_MINUS_DST_ALPHA`      | 1-A<sub>D</sub>, 1-A<sub>D</sub>, 1-A<sub>D</sub>                                                                   | 1-A<sub>D</sub> | Multiplies all colors by 1 minus the destination alpha color.                                                                                                      |
| `gl.CONSTANT_COLOR`           | R<sub>C</sub>, G<sub>C</sub>, B<sub>C</sub>                                                                         | A<sub>C</sub>   | Multiplies all colors by a constant color.                                                                                                                         |
| `gl.ONE_MINUS_CONSTANT_COLOR` | 1-R<sub>C</sub>, 1-G<sub>C</sub>, 1-B<sub>C</sub>                                                                   | 1-A<sub>C</sub> | Multiplies all colors by 1 minus a constant color.                                                                                                                 |
| `gl.CONSTANT_ALPHA`           | A<sub>C</sub>, A<sub>C</sub>, A<sub>C</sub>                                                                         | A<sub>C</sub>   | Multiplies all colors by a constant alpha value.                                                                                                                   |
| `gl.ONE_MINUS_CONSTANT_ALPHA` | 1-A<sub>C</sub>, 1-A<sub>C</sub>, 1-A<sub>C</sub>                                                                   | 1-A<sub>C</sub> | Multiplies all colors by 1 minus a constant alpha value.                                                                                                           |
| `gl.SRC_ALPHA_SATURATE`       | min(A<sub>S</sub>, 1 - A<sub>D</sub>), min(A<sub>S</sub>, 1 - A<sub>D</sub>), min(A<sub>S</sub>, 1 - A<sub>D</sub>) | 1               | Multiplies the RGB colors by the smaller of either the source alpha color or the value of 1 minus the destination alpha color. The alpha value is multiplied by 1. |

## Examples

To use the blend function, you first have to activate blending with
{{domxref("WebGLRenderingContext.enable()")}} with the argument `gl.BLEND`.

```js
gl.enable(gl.BLEND);
gl.blendFuncSeparate(gl.SRC_COLOR, gl.DST_COLOR, gl.ONE, gl.ZERO);
```

To get the current blend function, query the `BLEND_SRC_RGB`,
`BLEND_SRC_ALPHA`, `BLEND_DST_RGB`, and
`BLEND_DST_ALPHA` constants which return one of the blend function constants.

```js
gl.enable(gl.BLEND);
gl.blendFuncSeparate(gl.SRC_COLOR, gl.DST_COLOR, gl.ONE, gl.ZERO);
gl.getParameter(gl.BLEND_SRC_RGB) == gl.SRC_COLOR;
// true
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("WebGLRenderingContext.blendColor()")}}
- {{domxref("WebGLRenderingContext.blendEquation()")}}
