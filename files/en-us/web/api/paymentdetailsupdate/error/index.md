---
title: PaymentDetailsUpdate.error
slug: Web/API/PaymentDetailsUpdate/error
tags:
  - API
  - Error
  - Payment Request
  - Payment Request API
  - PaymentDetailsUpdate
  - Property
  - Reference
  - payment
browser-compat: api.PaymentDetailsUpdate.error
---
{{securecontext_header}}{{APIRef("Payment Request API")}}{{Deprecated_header}}{{Non-standard_header}}

The {{domxref("PaymentDetailsUpdate")}} dictionary's
**`error`** property is a human-readable
{{domxref("DOMString")}} which provides an error message to be displayed if the
specified information doesn't offer any valid shipping options.

## Syntax

```js
errorString = paymentDetailsUpdate.error;

paymentDetailsUpdate.error = errorString;
```

### Value

A {{domxref("DOMString")}} specifying the string to display to the user if the
information specified in the `PaymentDetailsUpdate` doesn't provide any valid
shipping options. This happens if both of the following are true:

- The {{domxref("PaymentRequest")}} specifies using its
  {{domxref("PaymentRequest.requestShipping", "requestShipping")}} property that
  shipping information is required.
- The {{domxref("PaymentDetailsUpdate")}} object specifies no valid shipping options
  in its {{domxref("PaymentDetailsUpdate.shippingOptions", "shippingOptions")}} list.

This message can be used to explain to the user why they cannot submit their payment as
currently specified—whether that's because the selected products cannot be shipped to
their region or because their address is not served by any of the shipping companies you
use.

## Browser compatibility

{{Compat}}
