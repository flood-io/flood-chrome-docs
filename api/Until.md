-------
# `Until`

Until is used to create wait <[Conditions]> which are used to wait for elements to become active, visible, invisible or disabled on the page.

You would typically use these to control the flow of you test.

#### `Until.ableToSwitchToFrame()`
* returns: <[Condition]> 

Creates a condition that will wait until the input driver is able to switch to the designated frame.

The target frame may be specified as:
- numeric index into window.frames for the currently selected frame.
- ElementHandle, which must references a FRAME or IFRAME element on the current page.
- locator which may be used to first locate a FRAME or IFRAME on the current page before attempting to switch to it.

Upon successful resolution of this condition, the driver will be left focused on the new frame.

#### `Until.alertIsPresent(alertText)`
* `alertText` <string>  
* returns: <[Condition]> 

Creates a condition that waits for an alert to be opened. Upon success, the returned promise will be fulfilled with the handle for the opened alert

#### `Until.elementIsDisabled(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to be disabled

#### `Until.elementIsEnabled(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to be enabled

#### `Until.elementIsNotSelected(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to be in the DOM, yet not visible to the user

#### `Until.elementIsNotVisible(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to become visible.

Example:
```typescript
step("Step 1", async browser => {
	 await browser.click(By.css('.hide-panel'))
  await browser.wait(Until.elementIsNotVisible(By.id("btn")))
})
```

#### `Until.elementIsSelected(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to be deselected.

#### `Until.elementIsVisible(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to be selected.

Example:
```typescript
step("Step 1", async browser => {
  await browser.wait(Until.elementIsVisible(By.partialLinkText("Start")))
})
```

#### `Until.elementLocated(locatable)`
* `locatable` <[Locatable]>  
* returns: <[Condition]> 

Creates a condition which will wait until the element is located on the page.

#### `Until.elementTextContains(locatable, text)`
* `locatable` <[Locatable]>  
* `text` <string>  
* returns: <[Condition]> 

Creates a condition which will wait until the element's text content contains the target text.

#### `Until.elementTextIs(locatable, text)`
* `locatable` <[Locatable]>  
* `text` <string>  
* returns: <[Condition]> 

Creates a condition which will wait until the element's text exactly matches the target text, excluding leading and trailing whitespace.

#### `Until.elementTextMatches(locatable, regex)`
* `locatable` <[Locatable]>  
* `regex` <[RegExp]>  
* returns: <[Condition]> 

Creates a condition which will wait until the element's text matches the target Regular Expression.

#### `Until.elementsLocated(selectorOrLocator)`
* `selectorOrLocator` <[Locator]|string>  
* returns: <[Condition]> 

Creates a condition that will loop until at least one element is found with the given locator.

#### `Until.stalenessOf(selectorOrLocator)`
* `selectorOrLocator` <[Locator]|string>  
* returns: <[Condition]> 

Creates a condition that will wait for the given element to become stale.

An element is considered stale once it is removed from the DOM, or a new page has loaded.

#### `Until.titleContains(title)`
* `title` <string>  
* returns: <[Condition]> 

Creates a condition which waits until the page title contains the expected text.

#### `Until.titleIs(title)`
* `title` <string>  
* returns: <[Condition]> 

Creates a condition which waits until the page title exactly matches the expected text.

#### `Until.titleMatches(title)`
* `title` <[RegExp]>  
* returns: <[Condition]> 

Creates a condition which waits until the page title matches the title `RegExp`.

#### `Until.urlContains(url)`
* `url` <string>  
* returns: <[Condition]> 

Creates a condition which waits until the page URL contains the expected path.

#### `Until.urlIs(url)`
* `url` <string>  
* returns: <[Condition]> 

Creates a condition which waits until the page URL exactly matches the expected URL.

#### `Until.urlMatches(url)`
* `url` <[RegExp]>  
* returns: <[Condition]> 

Creates a condition which waits until the page URL matches the supplied `RegExp`.


Until is used to create wait <[Conditions]> which are used to wait for elements to become active, visible, invisible or disabled on the page.

You would typically use these to control the flow of you test.


[Condition]: Condition.md
[Locatable]: Types.md