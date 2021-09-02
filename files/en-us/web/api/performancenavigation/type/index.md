---
title: PerformanceNavigation.type
slug: Web/API/PerformanceNavigation/type
tags:
  - API
  - Backwards compatibility
  - Deprecated
  - Navigation Timing
  - PerformanceNavigation
  - Property
  - Read-only
  - legacy
browser-compat: api.PerformanceNavigation.type
---
{{APIRef("Navigation Timing")}}{{Deprecated_Header}}

The legacy
**`PerformanceNavigation.type`**
read-only property returns an `unsigned short` containing a constant
describing how the navigation to this page was done.

> **Warning:** This interface of this property is deprecated in the [Navigation Timing Level 2 specification](https://w3c.github.io/navigation-timing/#obsolete).
> Please use the {{domxref("PerformanceNavigationTiming")}} interface instead.

Possible values are:

| Value | Constant name       | Meaning                                                                                                                   |
| ----- | ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `0`   | `TYPE_NAVIGATE`     | The page was accessed by following a link, a bookmark, a form submission, a script, or typing the URL in the address bar. |
| `1`   | `TYPE_RELOAD`       | The page was accessed by clicking the Reload button or via the {{domxref("Location.reload()")}} method.       |
| `2`   | `TYPE_BACK_FORWARD` | The page was accessed by navigating into the history.                                                                     |
| `255` | `TYPE_RESERVED`     | Any other way.                                                                                                            |

## Syntax

```js
type = performanceNavigation.type;
```

## Specifications

This feature is no longer on track to become a standard, as the [Navigation Timing specification](https://w3c.github.io/navigation-timing/#obsolete) has marked it as deprecated.
Use the {{domxref("PerformanceNavigationTiming")}} interface instead.

## Browser compatibility

{{Compat}}

## See also

- The {{domxref("PerformanceNavigation")}} interface it belongs to.
