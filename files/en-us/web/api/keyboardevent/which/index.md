---
title: KeyboardEvent.which
slug: Web/API/KeyboardEvent/which
tags:
  - API
  - DOM
  - Deprecated
  - KeyboardEvent
  - Property
  - Read-only
  - Reference
browser-compat: api.KeyboardEvent.which
---
{{ APIRef("DOM Events") }} {{Deprecated_header}}

The **`which`** read-only property of the
{{domxref("KeyboardEvent")}} interface returns the numeric `keyCode` of the
key pressed, or the character code (`charCode`) for an alphanumeric key
pressed.

## Syntax

```js
var keyResult = event.which;
```

### Return value

- `keyResult` contains the numeric code for a particular key pressed,
  depending on whether an alphanumeric or non-alphanumeric key was pressed. Please see
  {{domxref("KeyboardEvent.charCode")}} and {{domxref("KeyboardEvent.keyCode")}} for
  more details.

## Example

```html
<html>
<head>
<title>charCode/keyCode/which example</title>

<script type="text/javascript">

function showKeyPress(evt) {
alert("onkeypress handler: \n"
      + "keyCode property: " + evt.keyCode + "\n"
      + "which property: " + evt.which + "\n"
      + "charCode property: " + evt.charCode + "\n"
      + "Character Key Pressed: "
      + String.fromCharCode(evt.charCode) + "\n"
     );
}

function keyDown(evt) {
alert("onkeydown handler: \n"
      + "keyCode property: " + evt.keyCode + "\n"
      + "which property: " + evt.which + "\n"
     );
}

</script>
</head>

<body
 onkeypress="showKeyPress(event);"
 onkeydown="keyDown(event);"
>

<p>Please press any key.</p>

</body>
</html>
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("KeyboardEvent")}}, the interface this property belongs too.
