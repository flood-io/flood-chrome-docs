-------
# `ElementHandle`

Example Handle represents a remote element in the DOM of the browser. It implements useful methods for querying and interacting with this DOM element.

All methids on this class are asynchronous and must be used with `await` to wait for the result to fulfill from the browser.

#### `elementhandle.blur()`
* returns: <[Promise]<void>> 

Clears focus from this element so that it will no longer receive keyboard inputs.

#### `elementhandle.clear()`
* returns: <[Promise]<void>> 

Schedules a command to clear the value of this element.
This command has no effect if the underlying DOM element is neither a text
INPUT, SELECT, or a TEXTAREA element.

#### `elementhandle.click([, options])`
* `options` <[ClickOptions]> (Optional) 
* returns: <[Promise]<void>> 

Sends a click event to the element attached to this handle. If the element is
currently outside the viewport it will first scroll to that element.

#### `elementhandle.findElement(locator)`
* `locator` <string|[Locator]>  
* returns: <[Promise]<[ElementHandle]|null>> 

Locates an element using the supplied {@linkcode Locator}, returning an {@linkcode ElementHandle}

#### `elementhandle.findElements(locator)`
* `locator` <[Locator]|string>  
* returns: <[Promise]<[ElementHandle][]>> 

Locates all elements using the supplied {@linkcode Locator}, returning an array of {@linkcode ElementHandle}'s

#### `elementhandle.focus()`
* returns: <[Promise]<void>> 

Sends focus to this element so that it receives keyboard inputs.

#### `elementhandle.getAttribute(key)`
* `key` <string>  
* returns: <[Promise]<string|null>> 

Fetches the value of an attribute on this element

#### `elementhandle.getId()`
* returns: <[Promise]<string|null>> 

Fetches the remote elements `id` attribute.

#### `elementhandle.isDisplayed()`
* returns: <[Promise]<boolean>> 

Checks whether the remote element is displayed in the DOM and is visible to the user without being hidden by CSS or occluded by another element.

#### `elementhandle.isEnabled()`
* returns: <[Promise]<boolean>> 

Checks whether the remote element is enabled. Typically this means it does not have a `disabled` property or attribute applied.

#### `elementhandle.isSelectable()`
* returns: <[Promise]<boolean>> 

Checks whether the remote element is selectable. An element is selectable if it is an `<option>` or `input[type="checkbox"]` or radio button.

#### `elementhandle.isSelected()`
* returns: <[Promise]<boolean>> 

If the remote element is selectable (such as an `<option>` or `input[type="checkbox"]`) this methos will indicate whether it is selected.

#### `elementhandle.location()`
* returns: <[Promise]<>> 

Fetches the remote elements physical location as `x` and `y`.

#### `elementhandle.sendKeys(keys)`
* `keys` <string[]>  
* returns: <[Promise]<void>> 

#### `elementhandle.size()`
* returns: <[Promise]<>> 

Fetches the remote elements physical dimensions as `width` and `height`.

#### `elementhandle.tagName()`
* returns: <[Promise]<string|null>> 

Fetches the remote elements `tagName` property.

#### `elementhandle.takeScreenshot([, options])`
* `options` <[ScreenshotOptions]> (Optional) 
* returns: <[Promise]<void>> 

Takes a screenshot of this element and saves it to the results folder with a random name.

#### `elementhandle.text()`
* returns: <[Promise]<string>> 

Retrieves the text content of this element excluding leading and trailing whitespace.

#### `elementhandle.type(text)`
* `text` <string>  
* returns: <[Promise]<void>> 


Example Handle represents a remote element in the DOM of the browser. It implements useful methods for querying and interacting with this DOM element.

All methids on this class are asynchronous and must be used with `await` to wait for the result to fulfill from the browser.


[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[ClickOptions]: Interfaces.md
[Locator]: Locator.md
[ScreenshotOptions]: Interfaces.md