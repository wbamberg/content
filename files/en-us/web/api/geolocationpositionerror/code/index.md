---
title: GeolocationPositionError.code
slug: Web/API/GeolocationPositionError/code
tags:
  - API
  - Code
  - Geolocation API
  - GeolocationPositionError
  - Property
  - Secure context
browser-compat: api.GeolocationPositionError.code
---
{{securecontext_header}}{{APIRef("Geolocation API")}}

The **`GeolocationPositionError.code`** read-only property is
an `unsigned short` representing the error code.

## Syntax

```js
let typeErr = geolocationPositionErrorInstance.code
```

### Value

An `unsigned short` representing the error code. The following values are
possible:

| Value | Associated constant    | Description                                                                                                                                                                    |
| ----- | ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `1`   | `PERMISSION_DENIED`    | The acquisition of the geolocation information failed because the page didn't have the permission to do it.                                                                    |
| `2`   | `POSITION_UNAVAILABLE` | The acquisition of the geolocation failed because one or several internal sources of position returned an internal error.                                                      |
| `3`   | `TIMEOUT`              | The time allowed to acquire the geolocation, defined by {{domxref("PositionOptions.timeout")}} information that was reached before the information was obtained. |

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using geolocation](/en-US/docs/Web/API/Geolocation_API/Using_the_Geolocation_API)
- {{domxref("GeolocationPositionError")}}
