-------
# `BoundingBox`

* `height` <number>  The height.
* `width` <number>  The width.
* `x` <number>  The x-coordinate of top-left corner.
* `y` <number>  The y-coordinate of top-left corner.


-------
# `ClickOptions`

Specifies the available options to send when clicking to modify the click behaviour. For example, to send a double click, set `clickCount: 2`.

* `button` <[MouseButtons]> (Optional) defaults to left
* `clickCount` <number> (Optional) defaults to 1
* `delay` <number> (Optional) Time to wait between mousedown and mouseup in milliseconds.
Defaults to 0.

Specifies the available options to send when clicking to modify the click behaviour. For example, to send a double click, set `clickCount: 2`.


-------
# `NavigationOptions`

This interface represents the available options to pass to <[Driver]>.visit()

* `timeout` <number> (Optional) Maximum navigation time in milliseconds, pass 0 to disable timeout.
* `waitUntil` <load|domcontentloaded|networkidle0|networkidle2> (Optional) When to consider navigation succeeded.

This interface represents the available options to pass to <[Driver]>.visit()


-------
# `ScreenshotOptions`

Defines the screenshot options.

* `clip` <[BoundingBox]> (Optional) An object which specifies clipping region of the page.
* `fullPage` <boolean> (Optional) When true, takes a screenshot of the full scrollable page.
* `omitBackground` <boolean> (Optional) Hides default white background and allows capturing screenshots with transparency.
* `path` <string> (Optional) The file path to save the image to. The screenshot type will be inferred from file extension.
If `path` is a relative path, then it is resolved relative to current working directory.
If no path is provided, the image won't be saved to the disk.
* `quality` <number> (Optional) The quality of the image, between 0-100. Not applicable to png images.
* `type` <jpeg|png> (Optional) The screenshot type.

Defines the screenshot options.


[BoundingBox]: api/Interfaces.md
-------
# `StepOptions`

Specifies the available options which can be supplied to a step to override global settings.

**Example:**

```typescript
step("Step 1", { waitTimeout: 300 }, async browser => {
	await browser.click(...)
})
```

* `waitTimeout` <number> (Optional) Timeout in seconds for all wait and navigation operations within this <[step]>.

Specifies the available options which can be supplied to a step to override global settings.

**Example:**

```typescript
step("Step 1", { waitTimeout: 300 }, async browser => {
	await browser.click(...)
})
```


[step]: api/Functions.md
-------
# `TestSettings`

This interface specifies the available options you can use to configure how your test runs. These properties should be exported using the property `settings`.

**Example:**

```typescript
export const settings = {
  loopCount: Infinity,
  clearCache: true
}
```

* `DOMSnapshotOnFailure` <boolean> (Optional) Take a DOM snapshot of the page when a command fails, to aid in debugging.
* `actionDelay` <number> (Optional) Specifies the time (in seconds) to wait between each action call, to simulate a normal user
thinking about what to do next.
* `clearCache` <boolean> (Optional) Specifies whether Brwoser cache should be cleared after each loop.
* `clearCookies` <boolean> (Optional) Specifies whether cookies should be cleared after each loop.
* `description` <string> (Optional) Speicifies the description of the test specified in the comments section
* `device` <string> (Optional) Specifies a device to emulate with browser device emulation.
* `disableCache` <boolean> (Optional) Disables browser request cache for all requests.
* `duration` <number> (Optional) Maximum duration to run this for, regardless of other timeouts specified on Flood.

Defaults to `-1` for no timeout.
* `loopCount` <number> (Optional) Number of times to run this test.
Defaults to `-1` for infinite.
* `name` <string> (Optional) Speicifies the name of the test specified in the comments section
* `screenshotOnFailure` <boolean> (Optional) Take a screenshot of the page when a command fails, to aid in debugging.

Screenshots are saved to `/flood/result/screenshots` in the test archive.
* `stepDelay` <number> (Optional) Specifies the time (in seconds) to wait after each step.
* `userAgent` <string> (Optional) Specifies a custom User Agent (UA) string to send.
* `waitTimeout` <number> (Optional) Global wait timeout applied to all wait tasks

This interface specifies the available options you can use to configure how your test runs. These properties should be exported using the property `settings`.

**Example:**

```typescript
export const settings = {
  loopCount: Infinity,
  clearCache: true
}
```

