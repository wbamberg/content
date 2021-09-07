---
title: WebGL types
slug: Web/API/WebGL_API/Types
tags:
  - Reference
  - Types
  - WebGL
---
{{WebGLSidebar}}

The following types are used in [WebGL](/en-US/docs/Web/API/WebGL_API) interfaces.

## WebGL 1

These types are used within a {{domxref("WebGLRenderingContext")}}.

| Type         | Web IDL type         | Description                                                                                                                       |
| ------------ | -------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `GLenum`     | `unsigned long`      | Used for enums. See also the list of [constants](/en-US/docs/Web/API/WebGL_API/Constants).                                        |
| `GLboolean`  | `boolean`            | A boolean value.                                                                                                                  |
| `GLbitfield` | `unsigned long`      | A bit field that stores multiple, logical bits. Used for example in {{domxref("WebGLRenderingContext.clear()")}}. |
| `GLbyte`     | `byte`               | 8-bit twos complement signed integer.                                                                                             |
| `GLshort`    | `short`              | 16-bit twos complement signed integer.                                                                                            |
| `GLint`      | `long`               | 32-bit twos complement signed integer.                                                                                            |
| `GLsizei`    | `long`               | Used for sizes (e.g. width and height of the drawing buffer).                                                                     |
| `GLintptr`   | `long long`          | Special type for pointer arithmetic.                                                                                              |
| `GLsizeiptr` | `long long`          | Special type for pointer arithmetic.                                                                                              |
| `GLubyte`    | `octet`              | 8-bit twos complement unsigned integer.                                                                                           |
| `GLushort`   | `unsigned short`     | 16-bit twos complement unsigned integer.                                                                                          |
| `GLuint`     | `unsigned long`      | 32-bit twos complement unsigned integer.                                                                                          |
| `GLfloat`    | `unrestricted float` | 32-bit IEEE floating point number.                                                                                                |
| `GLclampf`   | `unrestricted float` | Clamped 32-bit IEEE floating point number.                                                                                        |

## WebGL 2

These types are used within a {{domxref("WebGL2RenderingContext")}}. All WebGL 1 types are used as well.

| Type      | Web IDL type | Description                   |
| --------- | ------------ | ----------------------------- |
| `GLint64` | `long long`  | Signed 64-bit integer number. |

## WebGL extensions

These types are used within [WebGL extensions](/en-US/docs/Web/API/WebGL_API/Using_Extensions).

| Type          | Web IDL type | Description                     |
| ------------- | ------------ | ------------------------------- |
| `GLuint64EXT` | `long long`  | Unsigned 64-bit integer number. |

## Specifications

| Specification                                                                    | Status                                           | Comment                   |
| -------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------------- |
| {{SpecName('WebGL', "#5.1", "Types")}}                             | {{Spec2('WebGL')}}                         | Initial definition        |
| {{SpecName('WebGL2', "#3.1", "Types")}}                             | {{Spec2('WebGL2')}}                         | Defines additional types. |
| {{SpecName('EXT_disjoint_timer_query', "", "GLuint64EXT")}} | {{Spec2('EXT_disjoint_timer_query')}} | Adds `GLuint64EXT`        |

## See also

- {{domxref("WebGLRenderingContext")}}
