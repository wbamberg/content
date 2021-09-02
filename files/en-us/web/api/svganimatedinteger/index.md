---
title: SVGAnimatedInteger
slug: Web/API/SVGAnimatedInteger
tags:
  - API
  - NeedsBrowserCompatibility
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGAnimatedInteger
---
{{APIRef("SVG")}}

## SVG animated integer interface

The `SVGAnimatedInteger` interface is used for attributes of basic type [\<integer>](/en-US/docs/SVG/Content_type#Integer) which can be animated.

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
          <li>readonly long <code>baseVal</code></li>
          <li>readonly long <code>animVal</code></li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedInteger"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type | Description                                                                                                                                                                                                                       |
| --------- | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `baseVal` | long | The base value of the given attribute before applying any animations.                                                                                                                                                             |
| `animVal` | long | If the given attribute or property is being animated, contains the current animated value of the attribute or property. If the given attribute or property is not currently being animated, contains the same value as `baseVal`. |

## Methods

The `SVGAnimatedInteger` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
