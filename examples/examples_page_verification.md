---
title: Examples - Page Verification
---

# Examples - Page Verification

## Overview

It is very important when load testing a target application that there is some form of page or object verification done with each step. This verification acts not only as a way to ensure you are on the correct page or part of the application but also serves to correctly calculate the response time for a step.

If you don't have a way of verifying the resultant page then you would just be timing the action of clicking on a link or button rather than taking into account the resulting page load and display time. 

## Complete string based page verification

The easiest way to verify that a resulting page has been load successfully is to check some static text value that you know will apear once the page is loaded.

```typescript
await browser.wait(Until.elementIsVisible(By.visibleText('Resulting page text here')))
```

We can use the *browser.wait* command along with the *By.visibleText* option containing the static text we would like to validate against.

## Partial string based page verification

You are also able to validate a resulting page using partial strings - as follows:

```typescript
		let pageTextVerify = By.partialVisibleText('Welcome to')
		await browser.wait(Until.elementIsVisible(pageTextVerify))
```

## User interface Object Verification

You are also able to wait for a specific object property on a resulting page load using a simple XPATH query.

```typescript
		let pageObjectVerify = By.xpath("//a[contains(@id, 'MyLoginLink')]")
		await browser.wait(Until.elementIsVisible(pageObjectVerify))
```