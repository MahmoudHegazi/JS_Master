# JS_Master
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
