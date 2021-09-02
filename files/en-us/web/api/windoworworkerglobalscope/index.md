---
title: WindowOrWorkerGlobalScope
slug: Web/API/WindowOrWorkerGlobalScope
tags:
  - API
  - HTML DOM
  - Service Worker
  - Window
  - WindowOrWorkerGlobalScope
  - Worker
  - WorkerGlobalScope
browser-compat: api.WindowOrWorkerGlobalScope
---
{{ApiRef()}}

The **`WindowOrWorkerGlobalScope`** mixin describes several features common to the {{domxref("Window")}} and {{domxref("WorkerGlobalScope")}} interfaces.

Each of these interfaces can, of course, add more features in addition to the ones listed below.

> **Note:** `WindowOrWorkerGlobalScope` is a mixin and not an interface; you can't actually create an object of type `WindowOrWorkerGlobalScope`.

## Properties

These properties are defined on the {{domxref("WindowOrWorkerGlobalScope")}} mixin, and implemented by {{domxref("Window")}} and {{domxref("WorkerGlobalScope")}}.

- {{domxref("caches")}} {{readOnlyinline}}
  - : Returns the {{domxref("CacheStorage")}} object associated with the current context. This object enables functionality such as storing assets for offline use, and generating custom responses to requests.
- {{domxref("crossOriginIsolated")}} {{readOnlyinline}}
  - : Returns a boolean value that indicates whether a {{jsxref("SharedArrayBuffer")}} can be sent via a {{domxref("Window.postMessage()")}} call.
- {{domxref("indexedDB")}} {{readonlyInline}}
  - : Provides a mechanism for applications to asynchronously access capabilities of indexed databases; returns an {{domxref("IDBFactory")}} object.
- {{domxref("isSecureContext")}} {{readOnlyinline}}
  - : Returns a boolean indicating whether the current context is secure (`true`) or not (`false`).
- {{domxref("origin")}} {{readOnlyinline}}
  - : Returns the origin of the global scope, serialized as a string.

## Methods

These methods are defined on the {{domxref("WindowOrWorkerGlobalScope")}} mixin, and implemented by {{domxref("Window")}} and {{domxref("WorkerGlobalScope")}}.

- {{domxref("atob", "atob()")}}
  - : Decodes a string of data which has been encoded using base-64 encoding.
- {{domxref("btoa", "btoa()")}}
  - : Creates a base-64 encoded ASCII string from a string of binary data.
- {{domxref("clearInterval()")}}
  - : Cancels the repeated execution set using {{domxref("setInterval()")}}.
- {{domxref("clearTimeout()")}}
  - : Cancels the delayed execution set using {{domxref("setTimeout()")}}.
- {{domxref("createImageBitmap()")}}
  - : Accepts a variety of different image sources, and returns a {{jsxref("Promise")}} which resolves to an {{domxref("ImageBitmap")}}. Optionally the source is cropped to the rectangle of pixels originating at _(_`sx`, `sy`_)_ with width `sw`, and height `sh`.
- {{domxref("fetch()")}}
  - : Starts the process of fetching a resource from the network.
- {{domxref("queueMicrotask()")}}
  - : Enqueues a microtask—a short function to be executed after execution of the JavaScript code completes and control isn't being returned to a JavaScript caller, but before handling callbacks and other tasks. This lets your code run without interfering with other, possibly higher priority, code, but _before_ the browser runtime regains control, potentially depending upon the work you need to complete.
- {{domxref("setInterval()")}}
  - : Schedules a function to execute every time a given number of milliseconds elapses.
- {{domxref("setTimeout()")}}
  - : Schedules a function to execute in a given amount of time.
- {{domxref("structuredClone()")}}
  - : Deep clone a JavaScript value using the structured clone algorithm.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("Window")}}
- {{domxref("WorkerGlobalScope")}}
