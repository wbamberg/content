---
title: CSS Painting API
slug: Web/API/CSS_Painting_API
tags:
  - API
  - CSS
  - CSS Paint API
  - Houdini
  - Painting
  - Reference
---
{{DefaultAPISidebar("CSS Painting API")}}

The CSS Painting API — part of the [CSS Houdini](/en-US/docs/Web/Houdini) umbrella of APIs — allows developers to write JavaScript functions that can draw directly into an element's background, border, or content.

## Concepts and usage

Essentially, the CSS Painting API contains functionality allowing developers to create custom values for {{cssxref('paint()', 'paint()')}}, a CSS [`<image>`](/en-US/docs/Web/CSS/image) function. You can then apply these values to properties like {{cssxref("background-image")}} to set complex custom backgrounds on an element.

For example:

```css
aside {
  background-image: paint(myPaintedImage);
}
```

The API defines {{domxref('PaintWorklet')}}, a {{domxref('worklet')}} that can be used to programmatically generate an image that responds to computed style changes. To find out more about how this is used, consult [Using the CSS Painting API](/en-US/docs/Web/API/CSS_Painting_API/Guide).

## Interfaces

- {{domxref('PaintWorklet')}}
  - : Programmatically generates an image where a CSS property expects a file. Access this interface through [`CSS.paintWorklet`](/en-US/docs/Web/API/CSS/paintWorklet "paintWorklet is a static, read-only property of the CSS interface that provides access to the PaintWorklet, which programmatically generates an image where a CSS property expects a file.").
- {{domxref('PaintWorkletGlobalScope')}}
  - : The global execution context of the `paintWorklet`.
- {{domxref('PaintRenderingContext2D')}}
  - : Implements a subset of the [CanvasRenderingContext2D API](/en-US/docs/Web/API/CanvasRenderingContext2D). It has an output bitmap that is the size of the object it is rendering to.
- {{domxref('PaintSize')}}
  - : Returns the read-only values of the output bitmap's width and height.

## Dictionaries

- {{domxref('PaintRenderingContext2DSettings')}}
  - : A dictionary providing a subset of [CanvasRenderingContext2D](/en-US/docs/Web/API/CanvasRenderingContext2D) settings.

## Examples

To draw directly into an element's background using JavaScript in our CSS, we define a paint worklet using the [`registerPaint()`](/en-US/docs/Web/API/PaintWorklet/registerPaint) function, tell the document to include the worklet using the paintWorklet addModule() method, then include the image we created using the CSS [`paint()`](</en-US/docs/Web/CSS/paint()>) function.

### Paint worklet

We create our PaintWorklet called 'hollowHighlights' using the [`registerPaint()`](/en-US/docs/Web/API/PaintWorklet/registerPaint) function:

```js
registerPaint('hollowHighlights', class {

  static get inputProperties() { return ['--boxColor']; }

  static get inputArguments() { return ['*','<length>']; }

  static get contextOptions() { return {alpha: true}; }

  paint(ctx, size, props, args) {
		const x = 0;
		const y = size.height * 0.3;
		const blockWidth = size.width * 0.33;
		const blockHeight = size.height * 0.85;

		const theColor = props.get( '--boxColor' );
		const strokeType = args[0].toString();
		const strokeWidth = parseInt(args[1]);

		console.log(theColor);

		if ( strokeWidth ) {
			ctx.lineWidth = strokeWidth;
		} else {
			ctx.lineWidth = 1.0;
		}

		if ( strokeType === 'stroke' ) {
			ctx.fillStyle = 'transparent';
			ctx.strokeStyle = theColor;
		} else if ( strokeType === 'filled' ) {
			ctx.fillStyle = theColor;
			ctx.strokeStyle = theColor;
		} else {
			ctx.fillStyle = 'none';
			ctx.strokeStyle = 'none';
		}

		ctx.beginPath();
		ctx.moveTo( x, y );
		ctx.lineTo( blockWidth, y );
		ctx.lineTo( blockWidth + blockHeight, blockHeight );
		ctx.lineTo( x, blockHeight );
		ctx.lineTo( x, y );
		ctx.closePath();
		ctx.fill();
		ctx.stroke();

		for (let i = 0; i < 4; i++) {
			let start = i * 2;
			ctx.beginPath();
			ctx.moveTo( blockWidth + (start * 10) + 10, y);
			ctx.lineTo( blockWidth + (start * 10) + 20, y);
			ctx.lineTo( blockWidth + (start * 10) + 20 + blockHeight, blockHeight);
			ctx.lineTo( blockWidth + (start * 10) + 10 + blockHeight, blockHeight);
			ctx.lineTo( blockWidth + (start * 10) + 10, y);
			ctx.closePath();
			ctx.fill();
			ctx.stroke();
		}
  }
});
```

### Using the paint worklet

We then include the paintWorklet:

```html
<ul>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
    <li>item 4</li>
    <li>item 5</li>
    <li>item 6</li>
    <li>item 7</li>
    <li>item 8</li>
    <li>item 9</li>
    <li>item 10</li>
    <li>item 11</li>
    <li>item 12</li>
    <li>item 13</li>
    <li>item 14</li>
    <li>item 15</li>
    <li>item 16</li>
    <li>item 17</li>
    <li>item 18</li>
    <li>item 19</li>
    <li>item 20</li>
</ul>
```

```js
  CSS.paintWorklet.addModule('https://mdn.github.io/houdini-examples/cssPaint/intro/worklets/hilite.js');
```

Then we can use the {{cssxref('&lt;image&gt;')}} with the CSS {{cssxref('paint()')}} function:

```css
li {
   --boxColor: hsla(55, 90%, 60%, 1.0);
   background-image: paint(hollowHighlights, stroke, 2px);
}

li:nth-of-type(3n) {
   --boxColor: hsla(155, 90%, 60%, 1.0);
   background-image: paint(hollowHighlights, filled,  3px);
}

li:nth-of-type(3n+1) {
   --boxColor: hsla(255, 90%, 60%, 1.0);
   background-image: paint(hollowHighlights, stroke, 1px);
}
```

We've included a custom property in the selector block defining a boxColor. Custom properties are accessible to the PaintWorklet.

### Result

{{EmbedLiveSample("Using_the_paint_worklet", 300, 300)}}

## Specifications

{{Specifications("api.PaintWorkletGlobalScope")}}

## Browser compatibility

See the browser compatibility data for each CSS Painting API Interface.

## See also

- [Using the CSS Painting API](/en-US/docs/Web/API/CSS_Painting_API/Guide)
- [CSS Typed Object Model API](/en-US/docs/Web/API/CSS_Typed_OM_API)
- [CSS Houdini](/en-US/docs/Web/Houdini)
