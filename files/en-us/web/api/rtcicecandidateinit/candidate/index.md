---
title: RTCIceCandidateInit.candidate
slug: Web/API/RTCIceCandidateInit/candidate
tags:
  - API
  - Candidate
  - ICE
  - Media
  - Property
  - RTCIceCandidateInit
  - SDP
  - Signaling
  - WebRTC
  - WebRTC API
  - candidate-attribute
browser-compat: api.RTCIceCandidateInit.candidate
---
{{APIRef("WebRTC")}}

The optional property **`candidate`** in the **{{domxref("RTCIceCandidateInit")}}** dictionary specifies the value of the {{domxref("RTCIceCandidate")}} object's {{domxref("RTCIceCandidate.candidate", "candidate")}} property.

## Value

<!-- this is the value that would have been set in /en-US/docs/Web/API/RTCIceCandidate/candidate-->

A {{domxref("DOMString")}} describing the properties of the candidate, taken directly
from the {{Glossary("SDP")}} attribute `"candidate"`. The candidate string
specifies the network connectivity information for the candidate. If the
`candidate` is an empty string (`""`), the end of the candidate
list has been reached; this candidate is known as the "end-of-candidates" marker.

The syntax of the candidate string is described in {{RFC(5245, "", 15.1)}}. For an
a-line (attribute line) that looks like this:

    a=candidate:4234997325 1 udp 2043278322 192.168.0.56 44323 typ host

the corresponding `candidate` string's value will be
`"candidate:4234997325 1 udp 2043278322 192.168.0.56 44323 typ host"`.

The {{Glossary("user agent")}} always prefers candidates with the highest
{{domxref("RTCIceCandidate.priority", "priority")}}, all else being equal. In the
example above, the priority is `2043278322`. The attributes are all separated
by a single space character, and are in a specific order. The complete list of
attributes for this example candidate is:

- {{domxref("RTCIceCandidate.foundation", "foundation")}} = 4234997325
- {{domxref("RTCIceCandidate.component", "component")}} = `"rtp"` (the
  number 1 is encoded to this string; 2 becomes `"rtcp"`)
- {{domxref("RTCIceCandidate.protocol", "protocol")}} = `"udp"`
- {{domxref("RTCIceCandidate.priority", "priority")}} = 2043278322
- {{domxref("RTCIceCandidate/address", "ip")}} = `"192.168.0.56"`
- {{domxref("RTCIceCandidate.port", "port")}} = 44323
- {{domxref("RTCIceCandidate.type", "type")}} = `"host"`

## Example

When a new ICE candidate is received by your signaling code from the remote peer, you need to construct the `RTCIceCandidate` object that encapsulates it. This is done in the event handler for the {{event("icecandidate")}} event. If your client-side signaling layer builds and transmits a JSON string including the candidate to the remote peer, the remote peer might handle receiving that JSON message like this:

```js
function gotICECandidateMessage(msg) {
  var iceCandidate = new RTCIceCandidate({
        candidate: msg.candidate;
  });

  pc.addIceCandidate(iceCandidate).catch({
    /* handle error */
  });
}
```

It's helpful to note that for backward compatibility with older versions of the WebRTC specification, the {{domxref("RTCIceCandidate.RTCIceCandidate", "RTCIceCandidate()")}} constructor accepts the value of `candidate` as its only input, in place of the `RTCIceCandidateInit` dictionary. That usage would change the above sample to look like this:

```js
function gotICECandidateMessage(msg) {
  var iceCandidate = new RTCIceCandidate(msg.candidate);

  pc.addIceCandidate(iceCandidate).catch({
    /* handle error */
  });
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [WebRTC API](/en-US/docs/Web/API/WebRTC_API)
- {{domxref("RTCIceCandidate.candidate")}}
- {{domxref("RTCPeerConnection.addIceCandidate()")}}
- {{event("icecandidate")}}
- [Lifetime of a WebRTC session](/en-US/docs/Web/API/WebRTC_API/Session_lifetime)
