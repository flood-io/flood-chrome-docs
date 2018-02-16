#### setup(settings)
* `settings` <`TestSettings`> 

* `returns:` <[void]> 

_This is a secondary syntax to `export const settings = {}` which functions exactly the same way.

**Example:**

```typescript
export default () => {
 setup({ waitTimeout: 60 })
}
```



#### step(name, fn)
* `name` <[string]> Step Name
* `fn` <`StepFunction`> Actual implementation of step

* `returns:` <[void]> 

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


#### step(name, options, fn)
* `name` <[string]> 
* `options` <`StepOptions`> 
* `fn` <`StepFunction`> 
* `returns:` <[void]> 


