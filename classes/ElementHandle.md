# ElementHandle
null
#### ElementHandle.blur()
* `returns:` <[Promise]> 

Clears focus from this element so that it will no longer receive keyboard inputs.

#### ElementHandle.clear()
* `returns:` <[Promise]> 

Schedules a command to clear the value of this element.
This command has no effect if the underlying DOM element is neither a text
INPUT, SELECT, or a TEXTAREA element.

#### ElementHandle.click(options)
* `options` <`ClickOptions`> 
* `returns:` <[Promise]> 

Sends a click event to the element attached to this handle. If the element is
currently outside the viewport it will first scroll to that element.

#### ElementHandle.findElement(locator)
* `returns:` <[Promise]> 

Locates an element using the supplied {@linkcode Locator}, returning an {@linkcode ElementHandle}

#### ElementHandle.findElements(locator)
* `returns:` <[Promise]> 

Locates all elements using the supplied {@linkcode Locator}, returning an array of {@linkcode ElementHandle}'s

#### ElementHandle.focus()
* `returns:` <[Promise]> 

Sends focus to this element so that it receives keyboard inputs.

#### ElementHandle.getAttribute(key)
* `key` <[string]> 
* `returns:` <[Promise]> 

Fetches the value of an attribute on this element

#### ElementHandle.getId()
* `returns:` <[Promise]> 



#### ElementHandle.isDisplayed()
* `returns:` <[Promise]> 



#### ElementHandle.isEnabled()
* `returns:` <[Promise]> 



#### ElementHandle.isSelectable()
* `returns:` <[Promise]> 



#### ElementHandle.isSelected()
* `returns:` <[Promise]> 



#### ElementHandle.location()
* `returns:` <[Promise]> 



#### ElementHandle.sendKeys(keys)
* `returns:` <[Promise]> 



#### ElementHandle.size()
* `returns:` <[Promise]> 



#### ElementHandle.tagName()
* `returns:` <[Promise]> 



#### ElementHandle.takeScreenshot(options)
* `options` <`ScreenshotOptions`> 
* `returns:` <[Promise]> 

Takes a screenshot of this element and saves it to the results folder with a random name.

#### ElementHandle.text()
* `returns:` <[Promise]> 

Retrieves the text content of this element excluding leading and trailing whitespace.

#### ElementHandle.type(text)
* `text` <[string]> 
* `returns:` <[Promise]> 




[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[Device]: Enumerations.md/#device