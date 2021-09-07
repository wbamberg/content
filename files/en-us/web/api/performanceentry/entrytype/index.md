---
title: PerformanceEntry.entryType
slug: Web/API/PerformanceEntry/entryType
tags:
  - API
  - Performance Timeline API
  - PerformanceEntry
  - Property
  - Reference
  - Web Performance
browser-compat: api.PerformanceEntry.entryType
---
{{APIRef("Performance Timeline API")}}

The **`entryType`** property returns
a {{domxref("DOMString")}} representing the type of performance metric such as, for
example, "`mark`". This property is read only.

{{AvailableInWorkers}}

## Syntax

```js
var type = entry.entryType;
```

### Return value

The return value depends on the subtype of the `PerformanceEntry` object and
affects the value of the {{domxref('PerformanceEntry.name')}} property as shown by the
table below.

### Performance entry type names

| Value                 | Subtype                                                                                                    | Type of name property            | Description of name property                                                                                                    |
| --------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `element`             | {{domxref('PerformanceElementTiming')}}                                                       | {{domxref("DOMString")}} | Reports load time of elements.                                                                                                  |
| `frame`, `navigation` | {{domxref('PerformanceFrameTiming')}}, {{domxref('PerformanceNavigationTiming')}} | {{domxref("URL")}}         | The document's address.                                                                                                         |
| `resource`            | {{domxref('PerformanceResourceTiming')}}                                                       | {{domxref("URL")}}         | The resolved URL of the requested resource. This value doesn't change even if the request is redirected.                        |
| `mark`                | {{domxref('PerformanceMark')}}                                                                   | {{domxref("DOMString")}} | The name used when the mark was created by calling {{domxref("Performance.mark","performance.mark()")}}.        |
| `measure`             | {{domxref('PerformanceMeasure')}}                                                               | {{domxref("DOMString")}} | name used when the measure was created by calling {{domxref("Performance.measure","performance.measure()")}}. |
| `paint`               | {{domxref('PerformancePaintTiming')}}                                                           | {{domxref("DOMString")}} | Either `'first-paint'` or `'first-contentful-paint'`.                                                                           |
| `longtask`            | {{domxref('PerformanceLongTaskTiming')}}                                                       | {{domxref("DOMString")}} | reports instances of long tasks                                                                                                 |

## Example

The following example shows the use of the `entryType` property.

```js
function run_PerformanceEntry() {

  // check for feature support before continuing
  if (performance.mark === undefined) {
    console.log("performance.mark not supported");
    return;
  }

  // Create a performance entry named "begin" via the mark() method
  performance.mark("begin");

  // Check the entryType of all the "begin" entries
  var entriesNamedBegin = performance.getEntriesByName("begin");
	for (var i=0; i < entriesNamedBegin.length; i++) {
      var typeOfEntry = entriesNamedBegin[i].entryType;
      console.log("Entry is type: " + typeOfEntry);
  }

}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
