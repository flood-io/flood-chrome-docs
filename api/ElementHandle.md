-------
# `ElementHandle`

Example Handle represents a remote element in the DOM of the browser. It implements useful methods for querying and interacting with this DOM element.

All methids on this class are asynchronous and must be used with `await` to wait for the result to fulfill from the browser.

#### `ElementHandle.blur()`
* returns: <Promise<void>> 

Clears focus from this element so that it will no longer receive keyboard inputs.

#### `ElementHandle.clear()`
* returns: <Promise<void>> 

Schedules a command to clear the value of this element.
This command has no effect if the underlying DOM element is neither a text
INPUT, SELECT, or a TEXTAREA element.

#### `ElementHandle.click([, options])`
* `options` <[ClickOptions]> (Optional) 
* returns: <Promise<void>> 

Sends a click event to the element attached to this handle. If the element is
currently outside the viewport it will first scroll to that element.

#### `ElementHandle.findElement(locator)`
* `locator` <string|[Locator]>  
* returns: <Promise<[ElementHandle]|null>> 

Locates an element using the supplied {@linkcode Locator}, returning an {@linkcode ElementHandle}

#### `ElementHandle.findElements(locator)`
* `locator` <[Locator]|string>  
* returns: <Promise<[ElementHandle][]>> 

Locates all elements using the supplied {@linkcode Locator}, returning an array of {@linkcode ElementHandle}'s

#### `ElementHandle.focus()`
* returns: <Promise<void>> 

Sends focus to this element so that it receives keyboard inputs.

#### `ElementHandle.getAttribute(key)`
* `key` <string>  
* returns: <Promise<string|null>> 

Fetches the value of an attribute on this element

#### `ElementHandle.getId()`
* returns: <Promise<string|null>> 

Fetches the remote elements `id` attribute.

#### `ElementHandle.isDisplayed()`
* returns: <Promise<boolean>> 

Checks whether the remote element is displayed in the DOM and is visible to the user without being hidden by CSS or occluded by another element.

#### `ElementHandle.isEnabled()`
* returns: <Promise<boolean>> 

Checks whether the remote element is enabled. Typically this means it does not have a `disabled` property or attribute applied.

#### `ElementHandle.isSelectable()`
* returns: <Promise<boolean>> 

Checks whether the remote element is selectable. An element is selectable if it is an `<option>` or `input[type="checkbox"]` or radio button.

#### `ElementHandle.isSelected()`
* returns: <Promise<boolean>> 

If the remote element is selectable (such as an `<option>` or `input[type="checkbox"]`) this methos will indicate whether it is selected.

#### `ElementHandle.location()`
* returns: <Promise<>> 

Fetches the remote elements physical location as `x` and `y`.

#### `ElementHandle.sendKeys(keys)`
* `keys` <string[]>  
* returns: <Promise<void>> 

#### `ElementHandle.size()`
* returns: <Promise<>> 

Fetches the remote elements physical dimensions as `width` and `height`.

#### `ElementHandle.tagName()`
* returns: <Promise<string|null>> 

Fetches the remote elements `tagName` property.

#### `ElementHandle.takeScreenshot([, options])`
* `options` <[ScreenshotOptions]> (Optional) 
* returns: <Promise<void>> 

Takes a screenshot of this element and saves it to the results folder with a random name.

#### `ElementHandle.text()`
* returns: <Promise<string>> 

Retrieves the text content of this element excluding leading and trailing whitespace.

#### `ElementHandle.type(text)`
* `text` <string>  
* returns: <Promise<void>> 


Example Handle represents a remote element in the DOM of the browser. It implements useful methods for querying and interacting with this DOM element.

All methids on this class are asynchronous and must be used with `await` to wait for the result to fulfill from the browser.


[ClickOptions]: api/Interfaces.md
[ScreenshotOptions]: api/Interfaces.md