---
title: WebSocket.readyState
slug: Web/API/WebSocket/readyState
tags:
  - API
  - Property
  - Reference
  - Web API
  - WebSocket
browser-compat: api.WebSocket.readyState
---
{{APIRef("Web Sockets API")}}

The **`WebSocket.readyState`** read-only property returns the
current state of the {{domxref("WebSocket")}} connection.

## Value

One of the following `unsigned short` values:

<table class="standard-table">
  <tbody>
    <tr>
      <td class="header">Value</td>
      <td class="header">State</td>
      <td class="header">Description</td>
    </tr>
    <tr>
      <td><code>0</code></td>
      <td><code>CONNECTING</code></td>
      <td>Socket has been created. The connection is not yet open.</td>
    </tr>
    <tr>
      <td><code>1</code></td>
      <td><code>OPEN</code></td>
      <td>The connection is open and ready to communicate.</td>
    </tr>
    <tr>
      <td><code>2</code></td>
      <td><code>CLOSING</code></td>
      <td>The connection is in the process of closing.</td>
    </tr>
    <tr>
      <td><code>3</code></td>
      <td><code>CLOSED</code></td>
      <td>The connection is closed or couldn't be opened.</td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
