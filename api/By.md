-------
# `By`

By is used to create <[Locator]>'s to find Elements or use in any place which accepts a Locator or <[Locatable]>.

#### `By.attr(tagName, attrName[, attrValue])`
* `tagName` <string>  TagName to scope selection to
* `attrName` <string>  The attribute to search for
* `attrValue` <string> (Optional) Optional attribute value to compare
* returns: <[Locator]> 

Finds an element containing a specified attribute value

#### `By.css(selector)`
* `selector` <string>  
* returns: <[Locator]> 

Locates an element using a CSS (jQuery) style selector

#### `By.id(id)`
* `id` <string>  
* returns: <[Locator]> 

Finds an element by ID

#### `By.js(func)`
* `func` <undefined>  
* returns: <[Locator]> 

Recives a function which runs on the page and returns an element or elements.

#### `By.linkText(text)`
* `text` <string>  
* returns: <[Locator]> 

Locates a link containing the specified text.

#### `By.partialLinkText(text)`
* `text` <string>  
* returns: <[Locator]> 

Locates a link (`<a>` tag) containing some of the specified text.

**Example:**
```typescript
await browser.findElement(By.partialLinkText("Checkout"))
```

#### `By.partialVisibleText(text)`
* `text` <string>  The substring to check for in a elements's visible text.
* returns: <[Locator]> 

Locates all elements whose `textContent` contains the given
substring and is not hidden by CSS.

#### `By.visibleText(text)`
* `text` <string>  The string to check for in a elements's visible text.
* returns: <[Locator]> 

Locates all elements whose `textContent` equals the given substring and is not hidden by CSS.

This selector works in multiple stages, by first finding the element matching the text predicate, and then testing whether it is visible ion the viewport and is not occluded by another element or style property.

#### `By.xpath(path)`
* `path` <string>  XPath selector
* returns: <[Locator]> 

Locates an element using an XPath expression


By is used to create <[Locator]>'s to find Elements or use in any place which accepts a Locator or <[Locatable]>.


[Locator]: ../Locator.md