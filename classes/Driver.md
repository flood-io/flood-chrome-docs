# Driver
Driver (also called Browser) is the main entry point in each [step],
it's your direct connection to the browser running the test.
#### Driver.blur(locator)
* `locator` <`Locatable`> 
* `returns:` <[Promise]> 



#### Driver.clear(locatable)
* `locatable` <`Locatable`> 
* `returns:` <[Promise]> 

Clears the selected value of an input or select control.

#### Driver.clearBrowserCache()
* `returns:` <[Promise]> 

Clear browser cache.

#### Driver.clearBrowserCookies()
* `returns:` <[Promise]> 

Clear browser cookies.

#### Driver.click(locatable, options)
* `locatable` <`Locatable`> 
* `options` <`ClickOptions`> 
* `returns:` <[Promise]> 

Sends a click event to the element located at `selector`. If the element is
currently outside the viewport it will first scroll to that element.

#### Driver.doubleClick(locatable, options)
* `locatable` <`Locatable`> 
* `options` <`ClickOptions`> 
* `returns:` <[Promise]> 

Sends a double-click event to the element located by the supplied Locator or `selector`. If the element is
currently outside the viewport it will first scroll to that element.

#### Driver.emulateDevice(deviceName)
* `deviceName` <[Device]> 
* `returns:` <[Promise]> 

Configure Browser to emulate a given device

#### Driver.findElement(locator)
* `returns:` <[Promise]> 

Uses the provided locator to find the first element it matches, returning an ElementHandle.

#### Driver.findElements(locator)
* `returns:` <[Promise]> 

Uses the provided locator to find all elements matching the locator condition, returning an array of ElementHandles

#### Driver.focus(locator)
* `locator` <`Locatable`> 
* `returns:` <[Promise]> 



#### Driver.press(keyCode, options)
* `keyCode` <[string]> 
* `returns:` <[Promise]> 



#### Driver.selectByIndex(locatable, index)
* `locatable` <`Locatable`> 
* `index` <[string]> 
* `returns:` <[Promise]> 

Selects an option within a `<select>` tag by its index in the list.

#### Driver.selectByText(locatable, text)
* `locatable` <`Locatable`> 
* `text` <[string]> 
* `returns:` <[Promise]> 

Selects an option within a `<select>` tag by matching its visible text.

#### Driver.selectByValue(locatable, values)
* `locatable` <`Locatable`> 
* `returns:` <[Promise]> 

Selects an option within a `<select>` tag using the value of the `<option>` element.

#### Driver.setUserAgent(userAgent)
* `userAgent` <[string]> 
* `returns:` <[Promise]> 

Set Browser to send a custom User Agent (UA) string

#### Driver.switchTo()
* `returns:` <`TargetLocator`> 

Switch the focus of the browser to another frame or window

#### Driver.takeScreenshot(options)
* `options` <`ScreenshotOptions`> 
* `returns:` <[Promise]> 

Takes a screenshot of the whole page and saves it to the results folder with a random sequential name.

#### Driver.type(locatable, text, options)
* `locatable` <`Locatable`> 
* `text` <[string]> 
* `returns:` <[Promise]> 

Types a string into an `<input>` control, key press by key press.

#### Driver.visit(url, options)
* `url` <[string]> 
* `options` <`NavigationOptions`> 
* `returns:` <[Promise]> 

Instructs the browser to navigate to a specific page. This is typically used as the
entrypoint to your test, as the first instruction it is also responsible for creating
a new Browser tab for this page to load into.

#### Driver.wait(timeoutOrCondition)
* `returns:` <[Promise]> 

You can use either a numeric value in seconds to wait for a specific time,
or a {@linkcode Condition}, for more flexible conditions.



[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[Device]: Enumerations.md/#device