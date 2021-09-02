---
title: SVGAnimatedBoolean
slug: Web/API/SVGAnimatedBoolean
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGAnimatedBoolean
---
{{APIRef("SVG")}}

## SVG animated boolean interface

The `SVGAnimatedBoolean` interface is used for attributes of type boolean which can be animated.

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
          <li>readonly boolean <code>baseVal</code></li>
          <li>readonly boolean <code>animVal</code></li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedBoolean"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type    | Description                                                                                                                                                                                                                       |
| --------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `baseVal` | boolean | The base value of the given attribute before applying any animations.                                                                                                                                                             |
| `animVal` | boolean | If the given attribute or property is being animated, contains the current animated value of the attribute or property. If the given attribute or property is not currently being animated, contains the same value as `baseVal`. |

## Methods

The `SVGAnimatedBoolean` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
