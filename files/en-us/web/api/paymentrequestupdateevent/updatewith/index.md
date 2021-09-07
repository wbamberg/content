---
title: PaymentRequestUpdateEvent.updateWith()
slug: Web/API/PaymentRequestUpdateEvent/updateWith
tags:
  - API
  - Change
  - Experimental
  - Method
  - Payment Change
  - Payment Details
  - Payment Request API
  - PaymentRequestUpdateEvent
  - Reference
  - Secure context
  - Web Payments
  - payment
  - updateWith
browser-compat: api.PaymentRequestUpdateEvent.updateWith
---
{{APIRef("Payment Request API")}}{{securecontext_header}}

The **`updateWith()`** method of the
{{domxref("PaymentRequestUpdateEvent")}} interface updates the details of an existing
{{domxref("PaymentRequest")}}.

## Syntax

```js
paymentRequestUpdateEvent.updateWith(details);
```

### Parameters

- `details`
  - : A {{domxref("PaymentDetailsUpdate")}} object specifying the changes applied to the
    payment request:
    {{page("/en-US/docs/Web/API/PaymentDetailsUpdate", "Properties")}}

### Return value

`undefined`.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
