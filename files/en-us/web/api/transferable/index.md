---
title: Transferable
slug: Web/API/Transferable
tags:
  - API
  - Interface
  - Reference
  - Transferable
  - Web Workers
browser-compat: api.Transferable
---
{{APIRef("DOM")}}

The **`Transferable`** interface represents an object that can be transfered between different execution contexts, like the main thread and Web workers.

This is an abstract interface and there is no object of this type. This interface does not define any method or property; it is merely a tag indicating objects that can be used in specific conditions, such as being transfered to a {{domxref("Worker")}} using the {{domxref("Worker.postMessage()")}} method.

> **Note:** The `Transferable` interface technically no longer exists. The _functionality_ of `Transferable` objects still exists, however, but is implemented at a more fundamental level (technically speaking, using the `[Transferable]` {{Glossary("WebIDL")}} extended attribute).

The {{jsxref("ArrayBuffer")}}, {{domxref("MessagePort")}}, {{domxref("ImageBitmap")}} and {{domxref("OffscreenCanvas")}} types implement this interface.

## Properties

_The `Transferable` interface does not implement or inherit specific properties._

## Methods

_The `Transferable` interface does not implement or inherit specific properties._

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- Interfaces implementing it: {{jsxref("ArrayBuffer")}}, {{domxref("MessagePort")}}, {{domxref("ImageBitmap")}}.
