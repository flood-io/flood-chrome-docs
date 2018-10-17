---
title: Handling Modal/Pop-up windows
---

# Detailed Example - Handling Modal/Pop-up windows

## Overview

This detailed example will show you how to handle randomly generated pop-up windows within your site that may be displayed for signing up to newsletters or displaying a special discount code which is fairly common with ecommerce websites and online stores.

With Flood Element it is possible to handle these sometimes randomly generated and often unexpected modal popups by putting in some validation checks in your script.

## Download the entire script

Please find the script used in this detailed scenario here: [link](https://gist.github.com/jrizio/106f5b36b1eee8c878c65e6be3a1ae86/archive/77a3ab58c746d0bcd91c1c0d40cbcc8d043f63fa.zip)

## Overview of script structure

Let's delve into how we can setup a script to handle these modal pop-ups:

a. **checkForModal function**

```typescript
async function checkForModal(browser) {
      //clear the modal if we get it after 5 seconds
      try {
		
		await browser.wait(Until.elementIsVisible(By.css('div > img')))
        let btnClose = await browser.findElement(By.css('div > img'))
		btnClose.click()
		
      } catch (error) {	
		console.log("The modal popup didn't appear this time.")
	  }
}
```
Here we define a function (called checkForModal) thats sole purpose is to check that an element of the modal pop-up is currently active and being displayed to the user. This function can be re-used in multiple steps depending on where you expect the pop-up to appear. You can also use this function on every step if your pop-up is randomly selected to appear at any time.

We've chosen the CSS selector for the close (x) button img which has it's selector as ```div > img```

If we don't see the close (x) button element then we simply log a message saying that we didn't see it within the expected timeframe.

b. **__checkForModal step**

```typescript
  step('__checkForModal1', { waitTimeout: 5 }, async browser => {
    await checkForModal(browser)
  })
```

This step can be added 1 or more times throughout your script. It will wait 5 seconds for the element to be visible before moving on to the next step. The beauty of having this in it's own step is that the 5 seconds max timeout will not affect your other step's transactiuon response time.

Please Note - you will need to name it __checkForModal1, __checkForModal2 ... __checkForModalx if you want to use them more than once. All steps need to be uniquely named otherwise they will be ignored.

c. **Putting it all together**

```typescript
export default () => {
  step('1. navigate to no modal page', { waitTimeout: 30 }, async browser => {  
    await browser.visit('https://jriz.io/modal/', { waitUntil: 'load' }) //test for no modal pop-up
  })

  step('__checkForModal1', { waitTimeout: 5 }, async browser => {
    await checkForModal(browser)
  })

  step('2. continue no modal', { waitTimeout: 30 }, async browser => {
    await browser.takeScreenshot()
  })  

  step('3. navigate to modal page', { waitTimeout: 30 }, async browser => {  
    await browser.visit('https://jriz.io/sample-page/', { waitUntil: 'load' }) //test for modal pop-up
  })

  step('__checkForModal2', { waitTimeout: 5 }, async browser => {
    await checkForModal(browser)
  })

  step('4. continue modal', { waitTimeout: 30 }, async browser => {
    await browser.takeScreenshot()
  })   
}
```
Here we have a full example of how we can use the checkForModal function with our normal steps.

Step 1 - navigates to a URL that does not display a modal pop-up. We place the __checkForModal1 step immediately after which will test to see that the modal appears within the specified 5 second timeout.
In this case we don't see a modal and continue onto the next step which will just capture a screenshot.

Step 3 - navigates to a URL that does display a 'signup to our newsletter' modal pop-up. We place second __checkForModal step to handle this pop-up. This time we do detect the presence of the pop-up and click on the close (x) button which clears the modal allowing our script to continue successfully.

d. **Execution Results**

Including one or more __checkForModal steps will also be displayed as part of your transaction labels when running the test through the Flood platform. These steps response times can be ignored as they aren't intended to be used to analyse response times but rather carry out the functionality to detect and clear the modal pop-ups. In a future version of Flood Element we will have the ability to mark these steps as 'Do not display' to make it clearer on the dashboard.

![Sample Execution Results](https://raw.githubusercontent.com/flood-io/flood-chrome-docs/master/examples/images/flood_checkmodal.png)

__checkForModal transactions are highlighted above and the applicable response times for these should be ignored as they are just displayed for completeness. As you can see __checkForModal1 shows a response time of ~5 seconds which is the timeout used to try and detect the close (x) button element.

## Conclusion

This is a very simple but effective way of handling unexpected modal pop-ups that are very common in e-commerce and online stores. They are a familiar tactic used to try and offer an incentive to the visitor to order from the site either now or at a future date.



