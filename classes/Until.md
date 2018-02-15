# Until
null
#### Until.ableToSwitchToFrame()
* `returns:` <`Condition`> 

Creates a condition that will wait until the input driver is able to switch to the designated frame.

#### Until.alertIsPresent(alertText)
* `alertText` <[string]> 

* `returns:` <`Condition`> 

Creates a condition that waits for an alert to be opened. Upon success, the returned promise will be fulfilled with the handle for the opened alert

#### Until.elementIsDisabled(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to be disabled

#### Until.elementIsEnabled(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to be enabled

#### Until.elementIsNotSelected(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to be in the DOM, yet not visible to the user

#### Until.elementIsNotVisible(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to become visible.

#### Until.elementIsSelected(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to be deselected.

#### Until.elementIsVisible(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to be selected.

#### Until.elementLocated(locatable)
* `locatable` <`Locatable`> 
* `returns:` <`Condition`> 

Creates a condition which will wait until the element is located on the page.

#### Until.elementTextContains(locatable, text)
* `locatable` <`Locatable`> 
* `text` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which will wait until the element's text content contains
the target text.

#### Until.elementTextIs(locatable, text)
* `locatable` <`Locatable`> 
* `text` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which will wait until the element's text exactly matches the target text,
excluding leading and trailing whitespace.

#### Until.elementTextMatches(locatable, regex)
* `locatable` <`Locatable`> 
* `regex` <`RegExp`> 
* `returns:` <`Condition`> 

Creates a condition which will wait until the element's text matches the target Regular Expression.

#### Until.elementsLocated(selectorOrLocator)
* `returns:` <`Condition`> 

Creates a condition that will loop until at least one element is found with the given locator.

#### Until.stalenessOf(selectorOrLocator)
* `returns:` <`Condition`> 

Creates a condition that will wait for the given element to become stale.
An element is considered stale once it is removed from the DOM, or a new page has loaded.

#### Until.titleContains(title)
* `title` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page title contains the expected text.

#### Until.titleIs(title)
* `title` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page title exactly matches the expected text.

#### Until.titleMatches(title)
* `title` <`RegExp`> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page title matches the title `RegExp`.

#### Until.urlContains(url)
* `url` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page URL contains the expected path.

#### Until.urlIs(url)
* `url` <[string]> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page URL exactly matches the expected URL.

#### Until.urlMatches(url)
* `url` <`RegExp`> 
* `returns:` <`Condition`> 

Creates a condition which waits until the page URL matches the supplied `RegExp`.


[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise