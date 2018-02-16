# ElementHandle
Example Handle represents a remote element in the DOM of the browser. It implements useful methods for querying and interacting with this DOM element.

All methids on this class are asynchronous and must be used with `await` to wait for the result to fulfill from the browser.

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

Fetches the remote elements `id` attribute.

#### ElementHandle.isDisplayed()
* `returns:` <[Promise]> 

Checks whether the remote element is displayed in the DOM and is visible to the user without being hidden by CSS or occluded by another element.

#### ElementHandle.isEnabled()
* `returns:` <[Promise]> 

Checks whether the remote element is enabled. Typically this means it does not have a `disabled` property or attribute applied.

#### ElementHandle.isSelectable()
* `returns:` <[Promise]> 

Checks whether the remote element is selectable. An element is selectable if it is an `<option>` or `input[type="checkbox"]` or radio button.

#### ElementHandle.isSelected()
* `returns:` <[Promise]> 

If the remote element is selectable (such as an `<option>` or `input[type="checkbox"]`) this methos will indicate whether it is selected.

#### ElementHandle.location()
* `returns:` <[Promise]> 

Fetches the remote elements physical location as `x` and `y`.

#### ElementHandle.sendKeys(keys)
* `returns:` <[Promise]> 



#### ElementHandle.size()
* `returns:` <[Promise]> 

Fetches the remote elements physical dimensions as `width` and `height`.

#### ElementHandle.tagName()
* `returns:` <[Promise]> 

Fetches the remote elements `tagName` property.

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




[Browser]: classes/Browser.md
[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[Device]: Enumerations.md/#device
[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[By]: classes/By.md
[Condition]: classes/Condition.md
[ElementHandle]: classes/ElementHandle.md