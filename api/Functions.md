#### `loadTestData(filePath)`
* `filePath` <string>  a path relative to root which contains the test data
* returns: <[Promise]<[TestDataRow][]>> 

Loads test data from the test directory to use in your test.

Supported formats:
- **CSV**: When loading CSV, you'll receive an array of objects for each row keyed by header
- **JSON**: When loading JSON, the root object should be an array of objects


[Promise]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
#### `setup(settings)`
* `settings` <[TestSettings]>  
* returns: <void> 

Declares the settings for the test, overriding settings exported at the top of the test.

_This is a secondary syntax to `export const settings = {}` which functions exactly the same way.

**Example:**

```typescript
export default () => {
 setup({ waitTimeout: 60 })
}
```


[TestSettings]: Interfaces.md#testsettings
#### `step(name, fn)`
* `name` <string>  Step Name
* `fn` <[StepFunction]>  Actual implementation of step
* returns: <void> 

Declares each step in your test. This must go within your main test expression.

**Example:**

```typescript
export default () => {
  step("Step 1", async browser => {
    await browser.visit("https://example.com")
  })

  step("Step 2", async browser => {})

  step("Step 3", async browser => {})
}
```

#### `step(name, options, fn)`
* `name` <string>  
* `options` <[StepOptions]>  
* `fn` <[StepFunction]>  
* returns: <void> 


[StepFunction]: Interfaces.md#stepfunction
[StepOptions]: Interfaces.md#stepoptions