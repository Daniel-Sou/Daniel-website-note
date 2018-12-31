# DOM Events with Javascript
Date on 31 Dec
---
## Review
Congrats, you completed the lesson! Now you've learned about JavaScript events and you can leverage these events on the DOM to create interactivity with event handlers.

Let's review what you've learned:

- JavaScript engines register events as objects with properties and methods associated with them.
- Event handlers are registered as properties of their event object.
- Event object properties like `.target `, ` .type `, and `.timeStamp` are used to provide information about the event.
- The `.addEventListener()` method can be used to add multiple event handler functions to a single event.
- The `.removeEventListener()` method stops specific event handlers from "listening" for specific events firing.

---

## Main Point
Event Handler Registration
```
let eventTarget = document.getElementById('targetElement');

eventTarget.onclick = function() {
  // this block of code will run
}
```

Second code:
```
let eventHandlerFunction = function() {
  // this block of code will run
}

eventTarget.onclick = eventHandlerFunction;
```

Adding Event Handler
```
let eventHandlerFunction = function() {
  // this block of code will run
}

eventTarget.onclick = eventHandlerFunction;
or
eventTarget.addEventListener('click', eventHandlerFunction);
```

Removing Event Handler
```
eventTarget.removeEventListener('click', eventHandlerFunction);

Example
eventTarget.addEventListener('event', function() {
target.removeEventListener('event', eventHandlerFunction);
})
```

Event Object Properties
```
let sharePhoto = function(event) {
  event.target.style.display = 'none';
  text.innerHTML = 'You share the puppy in ' 
  + event.timeStamp + ' ms.';
}

share.onclick = sharePhoto;
```
