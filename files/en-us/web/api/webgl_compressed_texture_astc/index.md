---
title: WEBGL_compressed_texture_astc
slug: Web/API/WEBGL_compressed_texture_astc
tags:
  - API
  - Reference
  - WebGL
  - WebGL extension
  - WebGL extensions
browser-compat: api.WEBGL_compressed_texture_astc
---
{{APIRef("WebGL")}}

The **`WEBGL_compressed_texture_astc`** extension is part of the [WebGL API](/en-US/docs/Web/API/WebGL_API) and exposes [Adaptive Scalable Texture Compression](https://en.wikipedia.org/wiki/Adaptive_Scalable_Texture_Compression) (ASTC) compressed texture formats to WebGL.

For more information, see the article [Using ASTC Texture Compression for Game Assets](https://developer.nvidia.com/astc-texture-compression-for-game-assets) by nvidia.

WebGL extensions are available using the {{domxref("WebGLRenderingContext.getExtension()")}} method. For more information, see also [Using Extensions](/en-US/docs/Web/API/WebGL_API/Using_Extensions) in the [WebGL tutorial](/en-US/docs/Web/API/WebGL_API/Tutorial).

> **Note:** ASTC compression is typically available on Mali ARM GPUs, Intel GPUs, and Nividia Tegra chips.
>
> This extension is available to both, {{domxref("WebGLRenderingContext", "WebGL1", "", 1)}} and {{domxref("WebGL2RenderingContext", "WebGL2", "", 1)}} contexts.

## Methods

This extension exposes one new methods.

- {{domxref("WEBGL_compressed_texture_astc.getSupportedProfiles", "ext.getSupportedProfiles()")}}
  - : Returns an array of strings containing the names of the ASTC profiles supported by the implementation.

## Constants

The compressed texture formats are exposed by 28 constants and can be used in two functions: {{domxref("WebGLRenderingContext.compressedTexImage2D", "compressedTexImage2D()")}} and {{domxref("WebGLRenderingContext.compressedTexSubImage2D", "compressedTexSubImage2D()")}}.

| Constants                                                                       | Blocks | Bits per pixel | {{jsxref("ArrayBuffer")}} `byteLength`               | bytes if height and width are 512 |
| ------------------------------------------------------------------------------- | ------ | -------------- | ----------------------------------------------------------- | --------------------------------- |
| `ext.COMPRESSED_RGBA_ASTC_4x4_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_4x4_KHR`     | 4x4    | 8.00           | `floor((width + 3) / 4) * floor((height + 3) / 4) * 16`     | 262144                            |
| `ext.COMPRESSED_RGBA_ASTC_5x4_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_5x4_KHR`     | 5x4    | 6.40           | `floor((width + 4) / 5) * floor((height + 3) / 4) * 16`     | 210944                            |
| `ext.COMPRESSED_RGBA_ASTC_5x5_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_5x5_KHR`     | 5x5    | 5.12           | `floor((width + 4) / 5) * floor((height + 4) / 5) * 16`     | 169744                            |
| `ext.COMPRESSED_RGBA_ASTC_6x5_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_6x5_KHR`     | 6x5    | 4.27           | `floor((width + 5) / 6) * floor((height + 4) / 5) * 16`     | 141728                            |
| `ext.COMPRESSED_RGBA_ASTC_6x6_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_6x6_KHR`     | 6x6    | 3.56           | `floor((width + 5) / 6) * floor((height + 5) / 6) * 16`     | 118336                            |
| `ext.COMPRESSED_RGBA_ASTC_8x5_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_8x5_KHR`     | 8x5    | 3.20           | `floor((width + 7) / 8) * floor((height + 4) / 5) * 16`     | 105472                            |
| `ext.COMPRESSED_RGBA_ASTC_8x6_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_8x6_KHR`     | 8x6    | 2.67           | `floor((width + 7) / 8) * floor((height + 5) / 6) * 16`     | 88064                             |
| `ext.COMPRESSED_RGBA_ASTC_8x8_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_8x8_KHR`     | 8x8    | 2.00           | `floor((width + 7) / 8) * floor((height + 7) / 8) * 16`     | 65536                             |
| `ext.COMPRESSED_RGBA_ASTC_10x5_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_10x5_KHR`   | 10x5   | 2.56           | `floor((width + 9) / 10) * floor((height + 4) / 5) * 16`    | 85696                             |
| `ext.COMPRESSED_RGBA_ASTC_10x6_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_10x6_KHR`   | 10x6   | 2.13           | `floor((width + 9) / 10) * floor((height + 5) / 6) * 16`    | 71552                             |
| `ext.COMPRESSED_RGBA_ASTC_10x8_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_10x8_KHR`   | 10x8   | 1.60           | `floor((width + 9) / 10) * floor((height + 7) / 8) * 16`    | 53248                             |
| `ext.COMPRESSED_RGBA_ASTC_10x10_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_10x10_KHR` | 10x10  | 1.28           | `floor((width + 9) / 10) * floor((height + 9) / 10) * 16`   | 43264                             |
| `ext.COMPRESSED_RGBA_ASTC_12x10_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_12x10_KHR` | 12x10  | 1.07           | `floor((width + 11) / 12) * floor((height + 9) / 10) * 16`  | 35776                             |
| `ext.COMPRESSED_RGBA_ASTC_12x12_KHR ext.COMPRESSED_SRGB8_ALPHA8_ASTC_12x12_KHR` | 12x12  | 0.89           | `floor((width + 11) / 12) * floor((height + 11) / 12) * 16` | 29584                             |

## Examples

```js
var ext = gl.getExtension('WEBGL_compressed_texture_astc');

var texture = gl.createTexture();
gl.bindTexture(gl.TEXTURE_2D, texture);

gl.compressedTexImage2D(gl.TEXTURE_2D, 0, ext.COMPRESSED_RGBA_ASTC_12x12_KHR, 512, 512, 0, textureData);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using ASTC Texture Compression for Game Assets](https://developer.nvidia.com/astc-texture-compression-for-game-assets)
- {{domxref("WebGLRenderingContext.getExtension()")}}
- {{domxref("WebGLRenderingContext.compressedTexImage2D()")}}
- {{domxref("WebGLRenderingContext.compressedTexSubImage2D()")}}
- {{domxref("WebGLRenderingContext.getParameter()")}}
