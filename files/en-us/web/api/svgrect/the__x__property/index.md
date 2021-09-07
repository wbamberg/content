---
title: The 'X' property
slug: Web/API/SVGRect/The__X__property
---
The [x](https://svgwg.org/svg2-draft/geometry.html#XProperty) property describes the horizontal coordinate of the position of the element.

## Usage context

| Name           | x                                                                                                                                                                                                                                                                                                                       |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Value          | [<length>](https://www.w3.org/TR/css3-values/#lengths) \| [<percentage>](https://www.w3.org/TR/css3-values/#percentages)                                                                                                                                                                                                |
| Initial        | 0                                                                                                                                                                                                                                                                                                                       |
| Applies to     | {{ SVGElement("mask") }} , ‘[svg](https://svgwg.org/svg2-draft/struct.html#SVGElement)’, ‘[rect](https://svgwg.org/svg2-draft/shapes.html#RectElement)’, ‘[image](https://svgwg.org/svg2-draft/embedded.html#ImageElement)’, ‘[foreignObject](https://svgwg.org/svg2-draft/embedded.html#ForeignObjectElement)’ |
| Inherited      | no                                                                                                                                                                                                                                                                                                                      |
| Percentages    | refer to the size of the current viewport (see [Units](https://svgwg.org/svg2-draft/coords.html#Units))                                                                                                                                                                                                                 |
| Media          | visual                                                                                                                                                                                                                                                                                                                  |
| Computed value | absolute length or percentage                                                                                                                                                                                                                                                                                           |
| Animatable     | yes                                                                                                                                                                                                                                                                                                                     |

## Simple usage

A \<coordinate> is a length in the user coordinate system that is the given distance from the origin of the user coordinate system along the relevant axis (the x-axis for X coordinates, the y-axis for Y coordinates). Its syntax is the same as that for [\<length>](https://www.w3.org/TR/SVG11/types.html#DataTypeLength)

    // Rect draws a rectangle with upper left-hand corner at x,y, with width w, and height h, with optional style
    // Standard Reference: http://www.w3.org/TR/SVG11/shapes.html#RectElement

         func (svg *SVG) Rect(x float64, y float64, w float64, h float64, s ...string) {
                 svg.printf(`<rect %s %s`, dim(x, y, w, h, svg.Decimals), endstyle(s, emptyclose))
    }
