#### setup(settings)
* `settings` <`TestSettings`> 

* `returns:` <[void]> 

Example: setup({ waitTimeout: 60 })



#### step(name, fn)
* `name` <[string]> Step Name
* `fn` <`StepFunction`> Actual implementation of step

* `returns:` <[void]> 

Declares each step in your test. This must go within the callback from `test()`.

#### step(name, options, fn)
* `name` <[string]> 
* `options` <`StepOptions`> 
* `fn` <`StepFunction`> 
* `returns:` <[void]> 


