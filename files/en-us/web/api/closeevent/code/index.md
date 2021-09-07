---
title: CloseEvent.code
slug: Web/API/CloseEvent/code
tags:
  - API
  - Property
  - Reference
  - closeEvent
browser-compat: api.CloseEvent.code
---
{{APIRef("Websockets API")}}

The **`code`** read-only property of the {{domxref("CloseEvent")}} interface returns the close code sent by the server.

### Value

A status code. As detailed in the following table, sourced from [the IANA website](https://www.iana.org/assignments/websocket/websocket.xml#close-code-number):

| Status code   | Name                       | Description                                                                                                                                                                                                    |
| ------------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `0`–`999`     |                            | **Reserved and not used.**                                                                                                                                                                                     |
| `1000`        | Normal Closure             | The connection successfully completed the purpose for which it was created.                                                                                                                                    |
| `1001`        | Going Away                 | The endpoint is going away, either because of a server failure or because the browser is navigating away from the page that opened the connection.                                                             |
| `1002`        | Protocol Error             | The endpoint is terminating the connection due to a protocol error.                                                                                                                                            |
| `1003`        | Unsupported Data           | The connection is being terminated because the endpoint received data of a type it cannot accept. (For example, a text-only endpoint received binary data.)                                                    |
| `1004`        |                            | **Reserved.** A meaning might be defined in the future.                                                                                                                                                        |
| `1005`        | No Status Received         | Indicates that no status code was provided even though one was expected.                                                                                                                                       |
| `1006`        | Abnormal Closure           | Indicates that a connection was closed abnormally (that is, with no close frame being sent) when a status code is expected.                                                                                    |
| `1007`        | Invalid frame payload data | The endpoint is terminating the connection because a message was received that contained inconsistent data (e.g., non-UTF-8 data within a text message).                                                       |
| `1008`        | Policy Violation           | The endpoint is terminating the connection because it received a message that violates its policy. This is a generic status code, used when codes 1003 and 1009 are not suitable.                              |
| `1009`        | Message too big            | The endpoint is terminating the connection because a data frame was received that is too large.                                                                                                                |
| `1010`        | Missing Extension          | The client is terminating the connection because it expected the server to negotiate one or more extension, but the server didn't.                                                                             |
| `1011`        | Internal Error             | The server is terminating the connection because it encountered an unexpected condition that prevented it from fulfilling the request.                                                                         |
| `1012`        | Service Restart            | The server is terminating the connection because it is restarting. [[Ref](https://www.ietf.org/mail-archive/web/hybi/current/msg09670.html)]                                                                   |
| `1013`        | Try Again Later            | The server is terminating the connection due to a temporary condition, e.g. it is overloaded and is casting off some of its clients. [[Ref](https://www.ietf.org/mail-archive/web/hybi/current/msg09670.html)] |
| `1014`        | Bad Gateway                | The server was acting as a gateway or proxy and received an invalid response from the upstream server. This is similar to 502 HTTP Status Code.                                                                |
| `1015`        | TLS Handshake              | **Reserved.** Indicates that the connection was closed due to a failure to perform a TLS handshake (e.g., the server certificate can't be verified).                                                           |
| `1016`–`1999` |                            | **Reserved for future use by the WebSocket standard.**                                                                                                                                                         |
| `2000`–`2999` |                            | **Reserved for use by WebSocket extensions.**                                                                                                                                                                  |
| `3000`–`3999` |                            | Available for use by libraries and frameworks. **May not** be used by applications. Available for registration at the IANA via first-come, first-serve.                                                        |
| `4000`–`4999` |                            | Available for use by applications.                                                                                                                                                                             |

> **Note:** The 1xxx codes are only WebSocket-internal and not for the same meaning by the transported data (like when the application-layer protocol is invalid). The only permitted codes to be specified in Firefox are 1000 and 3000 to 4999 \[[Source](https://searchfox.org/mozilla-central/rev/bf81d741ff5dd11bb364ef21306da599032fd479/dom/websocket/WebSocket.cpp#2533), [Bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1467107)].

## Examples

The following example prints the value of `code` to the console.

```js
WebSocket.onclose = function(event) {
  console.log(event.code);
};
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
