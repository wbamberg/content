---
title: 'Window: storage event'
slug: Web/API/Window/storage_event
tags:
  - API
  - Event
  - Reference
  - Storage
  - Web Storage
  - Window
browser-compat: api.Window.storage_event
---
{{APIRef}}

The **`storage`** event of the {{domxref("Window")}} interface fires when a storage area (`localStorage`) has been modified in the context of another document.

<table class="properties">
  <tbody>
    <tr>
      <th>Bubbles</th>
      <td>No</td>
    </tr>
    <tr>
      <th>Cancelable</th>
      <td>No</td>
    </tr>
    <tr>
      <th>Interface</th>
      <td>{{domxref("StorageEvent")}}</td>
    </tr>
    <tr>
      <th>Event handler property</th>
      <td>
        {{domxref("WindowEventHandlers.onstorage", "onstorage")}}
      </td>
    </tr>
  </tbody>
</table>

## Examples

Log the `sampleList` item to the console when the `storage` event fires:

```js
window.addEventListener('storage', () => {
  // When local storage changes, dump the list to
  // the console.
  console.log(JSON.parse(window.localStorage.getItem('sampleList')));
});
```

The same action can be achieved using the [`onstorage`](/en-US/docs/Web/API/WindowEventHandlers/onstorage) event handler property:

```js
window.onstorage = () => {
  // When local storage changes, dump the list to
  // the console.
  console.log(JSON.parse(window.localStorage.getItem('sampleList')));
};
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Web Storage API](/en-US/docs/Web/API/Web_Storage_API)
- [Using the Web Storage API](/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API)
