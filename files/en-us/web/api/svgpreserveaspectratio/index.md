---
title: SVGPreserveAspectRatio
slug: Web/API/SVGPreserveAspectRatio
tags:
  - API
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGPreserveAspectRatio
---
{{APIRef("SVG")}}

## SVG preserveAspectRatio interface

The `SVGPreserveAspectRatio` interface corresponds to the {{ SVGAttr("preserveAspectRatio") }} attribute, which is available for some of SVG's elements.

An `SVGPreserveAspectRatio` object can be designated as read only, which means that attempts to modify the object will result in an exception being thrown.

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
          <li>unsigned short <code>align</code></li>
          <li>unsigned short <code>meetOrSlice</code></li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Constants</th>
      <td>
        <ul>
          <li><code>SVG_PRESERVEASPECTRATIO_UNKNOWN</code> = 0</li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code
            ><code>_NONE</code> = 1
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code
            ><code>_XMINYMIN</code> = 2
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMIDYMIN</code> = 3
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMAXYMIN</code> = 4
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMINYMID</code> = 5
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMIDYMID</code> = 6
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMAXYMID</code> = 7
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMINYMAX</code> = 8
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMIDYMAX</code> = 9
          </li>
          <li>
            <code>SVG_</code><code>PRESERVEASPECTRATIO</code><code>_</code
            ><code>XMAXYMAX</code> = 10
          </li>
        </ul>
        <ul>
          <li><code>SVG_MEETORSLICE_UNKNOWN</code> = 0</li>
          <li>
            <code>SVG_</code><code>MEETORSLICE</code><code>_MEET</code> = 1
          </li>
          <li>
            <code>SVG_</code><code>MEETORSLICE</code><code>_SLICE</code> = 2
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a
          href="https://www.w3.org/TR/SVG/coords.html#InterfaceSVGPreserveAspectRatio"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Constants

| Name                                     | Value | Description                                                                                                                                                                                 |
| ---------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ` SVG_``PRESERVEASPECTRATIO``_UNKNOWN `  | 0     | The enumeration was set to a value that is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| ` SVG_``PRESERVEASPECTRATIO``_NONE `     | 1     | Corresponds to value `none` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                                 |
| ` SVG_``PRESERVEASPECTRATIO``_XMINYMIN ` | 2     | Corresponds to value `xMinYMin` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMIDYMIN ` | 3     | Corresponds to value `xMidYMin` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMAXYMIN ` | 4     | Corresponds to value `xMaxYMin` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMINYMID ` | 5     | Corresponds to value `xMinYMid` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMIDYMID ` | 6     | Corresponds to value `xMidYMid` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMAXYMID ` | 7     | Corresponds to value `xMaxYMid` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMINYMAX ` | 8     | Corresponds to value `xMinYMax` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMIDYMAX ` | 9     | Corresponds to value `xMidYMax` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| ` SVG_``PRESERVEASPECTRATIO``_XMAXYMAX ` | 10    | Corresponds to value `xMaxYMax` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                             |
| `SVG_MEETORSLICE_UNKNOWN`                | 0     | The enumeration was set to a value that is not one of predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type. |
| `SVG_MEETORSLICE_MEET`                   | 1     | Corresponds to value `meet` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                                 |
| `SVG_MEETORSLICE_SLICE`                  | 2     | Corresponds to value `slice` for attribute {{ SVGAttr("preserveAspectRatio") }}.                                                                                                |

## Properties

| Name          | Type           | Description                                                                                                                |
| ------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `align`       | unsigned short | The type of the alignment value as specified by one of the SVG*PRESERVEASPECTRATIO*\* constants defined on this interface. |
| `meetOrSlice` | unsigned short | The type of the meet-or-slice value as specified by one of the SVG*MEETORSLICE*\* constants defined on this interface.     |

**Exceptions on setting:** a [`DOMException`](DOMException) with code `NO_MODIFICATION_ALLOWED_ERR` is raised on an attempt to change the value of an attribute on a read only object.

## Methods

The `SVGPreserveAspectRatio` interface do not provide any specific methods.

## Browser compatibility

{{Compat}}
