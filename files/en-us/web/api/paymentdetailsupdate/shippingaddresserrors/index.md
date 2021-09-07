---
title: PaymentDetailsUpdate.shippingAddressErrors
slug: Web/API/PaymentDetailsUpdate/shippingAddressErrors
tags:
  - API
  - Address
  - Errors
  - Payment Request
  - Payment Request API
  - PaymentDetailsUpdate
  - Property
  - Reference
  - Shipping
  - Validation
  - payment
  - shippingAddressErrors
browser-compat: api.PaymentDetailsUpdate.shippingAddressErrors
---
{{APIRef("Payment Request API")}}{{securecontext_header}}{{Deprecated_header}}{{Non-standard_header}}

The {{domxref("PaymentDetailsUpdate")}} dictionary's
**`shippingAddressErrors`** property, if present,  contains an
{{domxref("AddressErrors")}} object whose contents provide error messages for one or
more of the values in the {{domxref("PaymentAddress")}} specified as
{{domxref("PaymentRequest.shippingAddress")}}.

## Syntax

```js
var addressErrors = PaymentDetailsUpdate.shippingAddressErrors;
```

### Value

An {{domxref("AddressErrors")}} object, which contains {{domxref("DOMString")}}s
describing errors in the properties of a {{domxref("PaymentAddress")}}. For each
property in `PaymentAddress`, a property by the same name is found in
`shippingAddressErrors` if and only if a validation error occurred for that
property. In that case, the property in `shippingAddressErrors` is a string
describing the validation error, ideally including suggestions about fixing the error.

## Browser compatibility

{{Compat}}
