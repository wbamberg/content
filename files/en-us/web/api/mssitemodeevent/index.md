---
title: MSSiteModeEvent
slug: Web/API/MSSiteModeEvent
---
{{Non-standard_header()}}

**`MSSiteModeEvent`** provides event properties that are specific to pinned site events.

This proprietary method is specific to Internet Explorer and Microsoft Edge.

### DOM Information

_Inheritance Hierarchy_

[Event](/en-US/docs/Web/API/Event)

MSSiteModeEvent

### Methods

| Method                     | Description                                                                                                                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `initEvent`                | Initializes a new generic event that the createEvent method created. \*_Note that as of Microsoft Edge, the `createEvent()/initEvent()` constructor pattern for synthetic events is deprecated._ |
| `preventDefault`           | Cancels the default action of an event.                                                                                                                                                          |
| `stopImmediatePropagation` | Prevents any further propagation of an event.                                                                                                                                                    |
| `stopPropagation`          | Prevents propagation of an event beyond the current target.                                                                                                                                      |

### Properties

| Property           | Description                                                                                                                       |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| `actionURL`        | Gets the URL of a Jump List item that is removed. \*_This property is not supported for Windows Store apps using JavaScript._     |
| `bubbles`          | Gets a value that indicates whether an event propagates up from the event target.                                                 |
| `buttonID`         | Gets the Thumbnail Toolbar button ID that is clicked. \*_This property is not supported for Windows Store apps using JavaScript._ |
| `cancelable`       | Gets a value that indicates whether you can cancel an event's default action.                                                     |
| `cancelBubble`     | Gets or sets a value that indicates whether an event should be stopped from propagating up from the current target.               |
| `currentTarget`    | Gets the event target that is currently being processed.                                                                          |
| `defaultPrevented` | Gets a value that indicates whether the default action should be canceled.                                                        |
| `eventPhase`       | Gets the event phase that is being evaluated.                                                                                     |
| `isTrusted`        | Gets a value that indicates whether a trusted event source created an event.                                                      |
| `srcElement`       | Gets the element that the event was originally dispatched to. Compare to _target_.                                                |
| `target`           | Gets the element that is the target of the event.                                                                                 |
| `timeStamp`        | Gets the time, in milliseconds, when an event occurred.                                                                           |
| `type`             | Gets the name of an event.                                                                                                        |

Although this event inherits from the [Event](/en-US/docs/Web/API/Event) object, it cannot be created by using [`createEvent`](/en-US/docs/Web/API/Document/createEvent).

## Example

    declare var MSSiteModeEvent: {
        prototype: MSSiteModeEvent;
        new(): MSSiteModeEvent;
    }

## See also

- [Microsoft API extensions](/en-US/docs/Web/API/Microsoft_Extensions)
