---
title: SVGAnimatedLength
slug: Web/API/SVGAnimatedLength
tags:
  - API
  - Reference
  - SVG
browser-compat: api.SVGAnimatedLength
---
{{APIRef("SVG")}}

## SVG animated length interface

The `SVGAnimatedLength` interface is used for attributes of basic type [\<length>](/en-US/docs/SVG/Content_type#Length) which can be animated.

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
            readonly {{ domxref("SVGLength") }} <code>baseVal</code>
          </li>
          <li>
            readonly {{ domxref("SVGLength") }} <code>animVal</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedLength"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type                                 | Description                                                                                                                                                                                                                       |
| --------- | ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `baseVal` | {{ domxref("SVGLength") }} | The base value of the given attribute before applying any animations.                                                                                                                                                             |
| `animVal` | {{ domxref("SVGLength") }} | If the given attribute or property is being animated, contains the current animated value of the attribute or property. If the given attribute or property is not currently being animated, contains the same value as `baseVal`. |

## Methods

The `SVGAnimatedLength` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
