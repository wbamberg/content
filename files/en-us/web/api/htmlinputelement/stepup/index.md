---
title: HTMLInputElement.stepUp()
slug: Web/API/HTMLInputElement/stepUp
tags:
  - API
  - HTML DOM
  - HTMLInputElement
  - Method
  - Reference
  - Text Field Selection API
browser-compat: api.HTMLInputElement.stepUp
---
{{APIRef("HTML DOM")}}

The **`HTMLInputElement.stepUp()`** method increments the value
of a numeric type of  {{HTMLElement("input")}} element by the value of the
[`step`](/en-US/docs/Web/HTML/Attributes/step) attribute, or the
default `step` value if the step attribute is not explicitly set. The method,
when invoked, increments the {{htmlattrxref("value","input")}} by
({{htmlattrxref("step","input")}} \* n), where `n` defaults to
`1` if not specified, and
[`step`](/en-US/docs/Web/HTML/Attributes/step) defaults to the
default value for `step` if not specified.

| Input type                                                                   | Default step value | Example step declaration                                                             |
| ---------------------------------------------------------------------------- | ------------------ | ------------------------------------------------------------------------------------ |
| {{HTMLElement("input/date", "date")}}                             | `1` (day)          | 7 day (one week) increments: `<input type="date" min="2019-12-25" step="7">`         |
| {{HTMLElement("input/month", "month")}}                         | `1` (month)        | 12 month (one year) increments: `<input type="month" min="2019-12" step="12">`       |
| {{HTMLElement("input/week", "week")}}                             | `1` (week)         | Two week increments: `<input type="week" min="2019-W23" step="2">`                   |
| {{HTMLElement("input/time", "time")}}                             | `60` (seconds)     | 900 second (15 minute) increments: `<input type="time" min="09:00" step="900">`      |
| {{HTMLElement("input/datetime-local", "datetime-local")}} | `1` (day)          | Same day of the week: `<input type="datetime-local" min="019-12-25T19:30" step="7">` |
| {{HTMLElement("input/number", "number")}}                     | `1`                | 0.1 increments `<input type="number" min="0" step="0.1" max="10">`                   |
| {{HTMLElement("input/range", "range")}}                         | `1`                | Increments by 2: `<input type="range" min="0" step="2" max="10">`                    |

The method, when invoked, changes the form control's value by the value given in the
`step` attribute, multiplied by the parameter, within the constraints set on
the form control. The default value for the parameter, if no value is passed, is
`1`. The method will not cause the value to exceed the
set [`max`](/en-US/docs/Web/HTML/Attributes/max) value, or defy
the constraints set by the
[`step`](/en-US/docs/Web/HTML/Attributes/step) attribute.

If the value before invoking the `stepUp()` method is invalid—for example,
if it doesn't match the constraints set by the step attribute—invoking the
`stepUp()` method will return a value that does match the form controls
constraints.

If the form control is non time, date, or numeric in nature, and therefore does not
support the `step` attribute (see the list of supported input types in the
table above), or if the step value is set to `any`, an
`InvalidStateError` exception is thrown.

## Syntax

```js
element.stepUp( [ stepIncrement ] );
```

### Parameters

- _`stepIncrement`_
  - : The optional  `stepIncrement` parameter is a numeric value.  If
    no parameter is passed, `stepIncrement` defaults to
    `1`.

## Example

Click the button in this example to increment the {{HTMLElement("input/number",
  "number")}} input type:

### HTML

```html
<p>
  <label>Enter a number between 0 and 400 that is divisible by 5:
   <input type="number" step="5" id="theNumber" min="0" max="400">
  </label>
</p>
<p>
  <label>Enter how many values of step you would like to increment by or leave it blank:
   <input type="number" step="1" id="incrementer" min="0" max="25">
  </label>
</p>
<input type="button" value="Increment" id="theButton">
```

### JavaScript

```js
/* make the button call the function */
let button = document.getElementById('theButton')
button.addEventListener('click', function() {
  steponup()
})

function steponup() {
  let input = document.getElementById('theNumber')
  let val = document.getElementById('incrementer').value

  if (val) {  /* increment with a parameter */
    input.stepUp(val)
  } else {    /* or without a parameter. Try it with 0 */
    input.stepUp()
  }
}
```

### CSS

```css
input:invalid {
  border: red solid 3px;
}
```

### Result

{{EmbedLiveSample("Example")}}

Note if you don't pass a parameter to the `stepUp` method, it defaults to
`1`. Any other value is a multiplier of the `step` attribute
value, which in this case is `5`. If you pass `4` as the
`stepIncrement`, the input will `stepUp` by
`4 * 5`, or `20`. If the parameter is `0`, the number
will not be incremented. The stepUp will not allow the input to out of range, in this
case stopping when it reaches `400`, and rounding down any floats that are
passed as a parameter.

Try setting the step increment to `1.2`. What happens when you invoke the
method?

Try setting the value to `4`, which is not valid. What happens when you
invoke the method?

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{HTMLElement("input")}}
- {{domxref("HTMLInputElement")}}
- {{domxref("HTMLInputElement.stepDown")}}
- [`step`](/en-US/docs/Web/HTML/Attributes/step),
  [`min`](/en-US/docs/Web/HTML/Attributes/min) and
  [`max`](/en-US/docs/Web/HTML/Attributes/max) attributes
