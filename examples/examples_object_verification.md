---
title: Examples - Page Verification
---

# Examples - Object Verification

## Using XPATH

You are also able to wait for a specific object property on a resulting page load using a simple XPATH query.

```typescript
		let pageObjectVerify = By.xpath("//a[contains(@id, 'MyLoginLink')]")
		await browser.wait(Until.elementIsVisible(pageObjectVerify))
```