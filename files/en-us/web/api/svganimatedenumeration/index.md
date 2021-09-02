---
title: SVGAnimatedEnumeration
slug: Web/API/SVGAnimatedEnumeration
tags:
  - API
  - NeedsExample
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGAnimatedEnumeration
---
{{APIRef("SVG")}}

## SVG animated enumeration interface

The `SVGAnimatedEnumeration` interface is used for attributes whose value must be a constant from a particular enumeration and which can be animated.

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
          <li>unsigned short <code>baseVal</code></li>
          <li>readonly unsigned short <code>animVal</code></li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG11/types.html#InterfaceSVGAnimatedEnumeration"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name      | Type           | Description                                                                                                                                                                                                                       |
| --------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `baseVal` | unsigned short | The base value of the given attribute before applying any animations.                                                                                                                                                             |
| `animVal` | unsigned short | If the given attribute or property is being animated, contains the current animated value of the attribute or property. If the given attribute or property is not currently being animated, contains the same value as `baseVal`. |

## Methods

The `SVGAnimatedEnumeration` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
