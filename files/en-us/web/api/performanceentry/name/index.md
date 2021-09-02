---
title: PerformanceEntry.name
slug: Web/API/PerformanceEntry/name
tags:
  - API
  - Property
  - Reference
  - Web Performance
browser-compat: api.PerformanceEntry.name
---
{{APIRef("Performance Timeline API")}}

The **`name`** property of the
{{domxref("PerformanceEntry")}} interface returns a value that further specifies the
value returned by the {{domxref("PerformanceEntry.entryType")}} property. This
property is read only.

{{AvailableInWorkers}}

## Syntax

```js
var name = entry.name;
```

### Return value

The return value depends on the subtype of the `PerformanceEntry` object and
the value of {{domxref("PerformanceEntry.entryType")}}, as shown by the table below.

| Value                            | Subtype                                                                                                    | entryType values      | Description                                                                                                                     |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| {{domxref("URL")}}         | {{domxref('PerformanceFrameTiming')}}, {{domxref('PerformanceNavigationTiming')}} | `frame`, `navigation` | The document's address.                                                                                                         |
| {{domxref("URL")}}         | {{domxref('PerformanceResourceTiming')}}                                                       | `resource`            | The resolved URL of the requested resource. This value doesn't change even if the request is redirected.                        |
| {{domxref("DOMString")}} | {{domxref('PerformanceMark')}}                                                                   | `mark`                | The name used when the mark was created by calling {{domxref("Performance.mark","performance.mark()")}}.        |
| {{domxref("DOMString")}} | {{domxref('PerformanceMeasure')}}                                                               | `measure`             | name used when the measure was created by calling {{domxref("Performance.measure","performance.measure()")}}. |
| {{domxref("DOMString")}} | {{domxref('PerformancePaintTiming')}}                                                           | `paint`               | Either `'first-paint'` or `'first-contentful-paint'`.                                                                           |

## Example

The following example shows the use of the `name` property.

```js
function run_PerformanceEntry() {
  log("PerformanceEntry support ...");

  if (performance.mark === undefined) {
    log("... performance.mark Not supported");
    return;
  }

  // Create some performance entries via the mark() method
  performance.mark("Begin");
  do_work(50000);
  performance.mark("End");

  // Use getEntries() to iterate through the each entry
  var p = performance.getEntries();
  for (var i=0; i < p.length; i++) {
    log("Entry[" + i + "]");
    check_PerformanceEntry(p[i]);
  }
}
function check_PerformanceEntry(obj) {
  var properties = ["name", "entryType", "startTime", "duration"];
  var methods = ["toJSON"];

  for (var i=0; i < properties.length; i++) {
    // check each property
    var supported = properties[i] in obj;
    if (supported)
      log("..." + properties[i] + " = " + obj[properties[i]]);
    else
      log("..." + properties[i] + " = Not supported");
  }
  for (var i=0; i < methods.length; i++) {
    // check each method
    var supported = typeof obj[methods[i]] == "function";
    if (supported) {
      var js = obj[methods[i]]();
      log("..." + methods[i] + "() = " + JSON.stringify(js));
    } else {
      log("..." + methods[i] + " = Not supported");
    }
  }
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
