---
title: SVGAnimatedRect
slug: Web/API/SVGAnimatedRect
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGAnimatedRect
---
{{APIRef("SVG")}}

The `SVGAnimatedRect` interface is used for attributes of basic {{ domxref("SVGRect") }} which can be animated.

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
            readonly {{ domxref("SVGRect") }} <code>baseVal</code>
          </li>
          <li>
            readonly {{ domxref("SVGRect") }} <code>animVal</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedRect"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type                             | Description                                                                                                                                                                                                                                                                                                                                                                                        |
| --------- | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `baseVal` | {{ domxref("SVGRect") }} | The base value of the given attribute before applying any animations.                                                                                                                                                                                                                                                                                                                              |
| `animVal` | {{ domxref("SVGRect") }} | A read only {{ domxref("SVGRect") }} representing the current animated value of the given attribute. If the given attribute is not currently being animated, then the {{ domxref("SVGRect") }} will have the same contents as `baseVal`. The object referenced by `animVal` will always be distinct from the one referenced by `baseVal`, even when the attribute is not animated. |

## Methods

_The `SVGAnimatedRect` interface do not provide any specific methods._

## Browser compatibility

{{Compat}}
