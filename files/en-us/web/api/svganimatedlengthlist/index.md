---
title: SVGAnimatedLengthList
slug: Web/API/SVGAnimatedLengthList
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGAnimatedLengthList
---
{{APIRef("SVG")}}

## SVG animated length list interface

The `SVGAnimatedLengthList` interface is used for attributes of type {{ domxref("SVGLengthList") }} which can be animated.

### Interface overview

<table class="standard-table">
  <tbody>
    <tr>
      <th scope="row">Also implement</th>
      <td><em>None</em></td>
    </tr>
    <tr>
      <th scope="row">Methods</th>
      <td><em>None</em></td>
    </tr>
    <tr>
      <th scope="row">Properties</th>
      <td>
        <ul>
          <li>
            readonly {{ domxref("SVGLengthList") }}
            <code>baseVal</code>
          </li>
          <li>
            readonly {{ domxref("SVGLengthList") }}
            <code>animVal</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedLengthList"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                        |
| --------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `baseVal` | {{ domxref("SVGLengthList") }} | The base value of the given attribute before applying any animations.                                                                                                                                                                                                                                                                                                                                              |
| `animVal` | {{ domxref("SVGLengthList") }} | A read only {{ domxref("SVGLengthList") }} representing the current animated value of the given attribute. If the given attribute is not currently being animated, then the {{ domxref("SVGLengthList") }} will have the same contents as `baseVal`. The object referenced by `animVal` will always be distinct from the one referenced by `baseVal`, even when the attribute is not animated. |

## Methods

The `SVGAnimatedLengthList` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
