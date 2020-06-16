# JS_Master

#use it (1) when:
So when would you want to use this technique? Well, 
JavaScript code in the <head> will run before JavaScript code in the <body>,
	so if you do have JavaScript code that needs to run as soon as possible,
	then you could put that code in the <head> and wrap it in a DOMContentLoaded event listener.
	This way it will run as early as possible, but not too early that the DOM isn't ready for it.

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="/css/styles.css" />
    <script>
      document.addEventListener('DOMContentLoaded', function () {
          document.querySelector('footer').style.backgroundColor = 'purple';
      });
    </script>
	
```	








This is for training, I used what I learned recently and added them all in one JS file that takes just 0.5400000372901559 ms to display the page and do a lot of JS codes (create 4 paragraphs, then append it to DocumentFragment () then create a div and append DocumentFragment to it, I also created (first post Switch (toggle) built in the world with 0 and 1 I created from the beginning I can copy logic very easily but I did not do it which is better the browser would say omg it's so easy can you make it harder please!, faster and easy to understood by the browser) Hide / show p , I used performance.now() in order to test the render time







--------------------------------------------------------------------------------------

```javascript
// Get the element, add a click listener...
document.getElementById("parent-list").addEventListener("click", function(e) {
	// e.target is the clicked element!
	// If it was a list item
	if(e.target && e.target.nodeName == "LI") {
		// List item found!  Output the ID!
		console.log("List item ", e.target.id.replace("post-", ""), " was clicked!");
	}
});
```

--------------------------------------------------------------------------------------

```javascript

// Get the parent DIV, add click listener...
document.getElementById("myDiv").addEventListener("click",function(e) {
	// e.target was the clicked element
  if (e.target && e.target.matches("a.classA")) {
    console.log("Anchor element clicked!");
	}
});
```

----------------------------------------------------------------------------------------
Using the Element.matches API, we can see if the element matches our desired target.

Since most developers use a JavaScript library for their DOM element and event handling, I recommend using the library's method of event delegation, as they are capable of advanced delegation and element identification.

Hopefully this helps you visually the concept behind event delegation and convinces you of delegation's power!





--------------------------------------------------------------------------------------------

The original target for this event is the Document that has loaded. You can listen for this event on the Window interface to handle it in the capture or bubbling phases. For full details on this event please see the page on the Document: DOMContentLoaded event.

A different event, load, should be used only to detect a fully-loaded page. It is a common mistake to use load where DOMContentLoaded would be more appropriate.

```javascript
Basic usage
window.addEventListener('DOMContentLoaded', (event) => {
    console.log('DOM fully loaded and parsed');
})
```

# why and when we use DOMContentLoaded event

```text
document.querySelector('footer').style.backgroundColor = 'purple';
Does anything jump out at you about this code? Anything at all?
This code is completely error-free...unfortunately, when it runs, 
it will still cause an error. Any ideas why?

The problem is with the .querySelector() method. When it runs...there's no <footer> 
element to select from the constructed document object model yet!
So instead of returning a DOM element, it will return null. 
This causes an error because it would be like running the following code:

Now, we've already used one solution to this issue.
Remember that we moved the JavaScript file down to the bottom of the page. 
Think about why this would make things work. Well, if the DOM is built sequentially, 
_if_ the JavaScript code is moved to the very bottom of the page, 
then by the time the JavaScript code is run, all DOM elements will already exist!

However, an alternative solution would be to use browser events! 🙌🏼


```

```javascript
document.addEventListener('DOMContentLoaded', function () {
    console.log('the DOM is ready to be interacted with!');
});

```

