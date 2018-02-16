# Browser

Browser (also called Driver) is the main entry point in each <[step]>, it's your direct connection to the browser running the test.

```typescript
import { step } from '@flood/chrome'
export default () => {
	step('Start', async browser => {
		await browser.visit('https://challenge.flood.io')
	})
}
```

#### Browser.blur(locator)

* `locator` <`Locatable`>
* `returns:` <[Promise]>

Removes focus from the specified DOM element.

#### Browser.clear(locatable)

* `locatable` <`Locatable`>
* `returns:` <[Promise]>

Clears the selected value of an input or select control.

#### Browser.clearBrowserCache()

* `returns:` <[Promise]>

Clear browser cache.

#### Browser.clearBrowserCookies()

* `returns:` <[Promise]>

Clear browser cookies.

#### Browser.click(locatable, options)

* `locatable` <`Locatable`>
* `options` <`ClickOptions`>
* `returns:` <[Promise]>

Sends a click event to the element located at `selector`. If the element is
currently outside the viewport it will first scroll to that element.

**Example:**

```typescript
step('Start', async browser => {
	await browser.click(By.partialLinkText('Start'))
})
```

In this example we're constructing a <[Locatable]> using the `By.partialLinkText()` Locator, which will match the first `<a>` tag which contains the text "Start".

#### Browser.doubleClick(locatable, options)

* `locatable` <`Locatable`>
* `options` <`ClickOptions`>
* `returns:` <[Promise]>

Sends a double-click event to the element located by the supplied Locator or `selector`. If the element is
currently outside the viewport it will first scroll to that element.

#### Browser.emulateDevice(deviceName)

* `deviceName` <[Device]>
* `returns:` <[Promise]>

Configure Browser to emulate a given device

#### Browser.findElement(locator)

* `returns:` <[Promise]>

Uses the provided locator to find the first element it matches, returning an ElementHandle.

#### Browser.findElements(locator)

* `returns:` <[Promise]>

Uses the provided locator to find all elements matching the locator condition, returning an array of ElementHandles

#### Browser.focus(locator)

* `locator` <`Locatable`> The <[Locator]> to use to find an element to send focus to.
* `returns:` <[Promise]>

Makes the element located by the first argument the receiver of future input.

#### Browser.press(keyCode, options)

* `keyCode` <[string]>
* `returns:` <[Promise]>

Presses a key on the keyboard specified by key code. For example, <[Key.ALT]>

#### Browser.selectByIndex(locatable, index)

* `locatable` <`Locatable`>
* `index` <[string]>
* `returns:` <[Promise]>

Selects an option within a `<select>` tag by its index in the list.

#### Browser.selectByText(locatable, text)

* `locatable` <`Locatable`>
* `text` <[string]>
* `returns:` <[Promise]>

Selects an option within a `<select>` tag by matching its visible text.

#### Browser.selectByValue(locatable, values)

* `locatable` <`Locatable`>
* `returns:` <[Promise]>

Selects an option within a `<select>` tag using the value of the `<option>` element.

#### Browser.setUserAgent(userAgent)

* `userAgent` <[string]>
* `returns:` <[Promise]>

Set Browser to send a custom User Agent (UA) string

#### Browser.switchTo()

* `returns:` <`TargetLocator`>

Switch the focus of the browser to another frame, tab, or window.

#### Browser.takeScreenshot(options)

* `options` <`ScreenshotOptions`>
* `returns:` <[Promise]>

Takes a screenshot of the whole page and saves it to the `flood/results` folder with a random sequential name. You can download the archive of your test results at the end of the test to retrieve these screenshots.

#### Browser.type(locatable, text, options)

* `locatable` <`Locatable`>
* `text` <[string]>
* `returns:` <[Promise]>

Types a string into an `<input>` control, key press by key press. Use this to fill inputs as though it was typed by the user.

**Example:**

```typescript
step('Step 1', async browser => {
	await browser.type(By.css('#email'), 'user@example.com')
})
```

#### Browser.visit(url, options)

* `url` <[string]>
* `options` <`NavigationOptions`>
* `returns:` <[Promise]>

Instructs the browser to navigate to a specific page. This is typically used as the
entrypoint to your test, as the first instruction it is also responsible for creating
a new Browser tab for this page to load into.

**Example:**

```typescript
step('Start', async browser => {
	await browser.visit('https://example.com')
})
```

#### Browser.wait(timeoutOrCondition)

* `returns:` <[Promise]>

Creates a waiter which will pause the test until a condition is met or a timeout is reached. This can be used for validation or control flow.

**Example:**

```typescript
step('Start', async browser => {
	await browser.wait(Until.elementIsVisible(By.css('h1.title')))
})
```

You can use either a numeric value in seconds to wait for a specific time,
or a {@linkcode Condition}, for more flexible conditions.

[browser]: classes/Browser.md
[promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[device]: Enumerations.md/#device
[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
