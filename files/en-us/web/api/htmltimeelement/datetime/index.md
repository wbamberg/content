---
title: HTMLTimeElement.dateTime
slug: Web/API/HTMLTimeElement/dateTime
tags:
  - API
  - HTML DOM
  - HTMLTimeElement
  - Property
  - Reference
browser-compat: api.HTMLTimeElement.dateTime
---
{{ APIRef("HTML DOM") }}

The
**`HTMLTimeElement.dateTime`**
property is a {{domxref("DOMString")}} that reflects the {{ htmlattrxref("datetime",
  "time") }} HTML attribute, containing a machine-readable form of the element's date and
time value.

The format of the string must follow one of the following HTML microsyntaxes:

| Microsyntax                       | Description                                                                                                                                                                                                                                                                                                      | Examples                                                                                                                              |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Valid month string                | _YYYY_`-`_MM_                                                                                                                                                                                                                                                                                                    | `2011-11`, `2013-05`                                                                                                                  |
| Valid date string                 | _YYYY_`-`_MM_`-`_DD_                                                                                                                                                                                                                                                                                             | `1887-12-01`                                                                                                                          |
| Valid yearless date string        | _MM_`-`_DD_                                                                                                                                                                                                                                                                                                      | `11-12`                                                                                                                               |
| Valid time string                 | _HH_`:`_MM_ _HH_`:`_MM_`:`_SS_ _HH_`:`_MM_`:`_SS_`.`_mmm_                                                                                                                                                                                                                                                        | `23:59` `12:15:47` `12:15:52.998`                                                                                                     |
| Valid local date and time string  | _YYYY_`-`_MM_`-`_DD_ _HH_`:`_MM_ _YYYY_`-`_MM_`-`_DD_ _HH_`:`_MM_`:`_SS_ _YYYY_`-`_MM_`-`_DD_ _HH_`:`_MM_`:`_SS_`.`_mmm_ _YYYY_`-`_MM_`-`_DD_`T`_HH_`:`_MM_ _YYYY_`-`_MM_`-`_DD_`T`_HH_`:`_MM_`:`_SS_ _YYYY_`-`_MM_`-`_DD_`T`_HH_`:`_MM_`:`_SS_`.`_mmm_                                                          | `2013-12-25 11:12 1972-07-25 13:43:07 1941-03-15 07:06:23.678 2013-12-25T11:12 1972-07-25T13:43:07 1941-03-15T07:06:23.678`           |
| Valid time-zone offset string     | `Z` `+`_HHMM_ `+`_HH_`:`_MM_ `-`_HHMM_ `-`_HH_`:`_MM_                                                                                                                                                                                                                                                            | `Z +0200 +04:30 -0300 -08:00`                                                                                                         |
| Valid global date and time string | _Any combination of a valid local date and time string followed by a valid time-zone offset string_                                                                                                                                                                                                              | `2013-12-25 11:12+0200 1972-07-25 13:43:07+04:30 1941-03-15 07:06:23.678Z 2013-12-25T11:12-08:00`                                     |
| Valid week string                 | _YYYY_`-W`_WW_                                                                                                                                                                                                                                                                                                   | `2013-W46`                                                                                                                            |
| Four or more ASCII digits         | _YYYY_                                                                                                                                                                                                                                                                                                           | `2013`, `0001`                                                                                                                        |
| Valid duration string             | `P`_d_` D``T `_h_`H`_m_`M`_s_`S` `P`_d_` D``T `_h_`H`_m_`M`_s_`.`X`S` `P`_d_` D``T `_h_`H`_m_`M`_s_`.`XX`S` `P`_d_` D``T `_h_`H`_m_`M`_s_`.`XXX`S` ` P``T `_h_`H`_m_`M`_s_`S` ` P``T `_h_`H`_m_`M`_s_`.`X`S` ` P``T `_h_`H`_m_`M`_s_`.`XX`S` ` P``T `_h_`H`_m_`M`_s_`.`XXX`S` _w_`w `_d_`d `_h_`h `_m_`m `_s_`s` | `P12DT7H12M13S P12DT7H12M13.3S P12DT7H12M13.45S P12DT7H12M13.455S PT7H12M13S PT7H12M13.2S PT7H12M13.56S PT7H12M13.999S 7d 5h 24m 13s` |

## Syntax

```js
dateTimeString = timeElt.dateTime;
timeElt.dateTime = dateTimeString
```

## Example

```js
// Assumes there is <time id="t"> element in the HTML

var t = document.getElementById("t");
t.dateTime = "6w 5h 34m 5s";
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The {{domxref("HTMLTimeElement")}} interface it belongs to.
