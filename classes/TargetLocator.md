# TargetLocator
null
#### TargetLocator.activeElement()
* `returns:` <[Promise]> 

Locates the DOM element on the current page that corresponds to
`document.activeElement` or `document.body` if the active element is not
available.

#### TargetLocator.defaultContent()
* `returns:` <[Promise]> 

Navigates to the topmost frame

#### TargetLocator.frame(id)
* `returns:` <[Promise]> 

Accepts either:

number: Switch to frame by index in window.frames,
string: Switch to frame by frame.name or frame.id, whichever matches first,
ElementHandle: Switch to a frame using the supplied ElementHandle of a frame.



[By]: classes/By.md
[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[Condition]: classes/Condition.md
[Driver]: classes/Driver.md
[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[Device]: Enumerations.md/#device
[ElementHandle]: classes/ElementHandle.md
[Locator]: classes/Locator.md
[TargetLocator]: classes/TargetLocator.md