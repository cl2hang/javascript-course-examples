# JavaScript

## Lesson 22 - Events

### 1. Recall

__HTML DOM__

* A tree based model of the HTML web page data in the browser
* Each HTML element is represented as a __tree node__. 
* The highest level node, corresponding to the __HTML__ element, is __`document`__
* use __`document.body`__ to refer to the __body__ element.
* use __`document.getElementById()`__ to refer to any element in the document by giving corresponding ID.

For any current tree node (suppose it's __`n`__), we can use the following method or attribute:
* __`n.innerHTML`__ to get or modify the encluded HTML content;
* use any HTML attribute name, like __`n.style`__, to modify the corresponding HTML attribute;
* use methods like __`n.firstChild`__, __`n.nextSibling` __, __`n.parentNode`__ to navigate in the tree.
* use methods __`document.createElement()`__ to create a node correspondgin to an HTML element, and __`document.createTextNode()`__ to create a text node.
* use method __`n.appendChild()`__ to add a newly created node to the children of the current tree node.

### 2. HTML Events

__Mouse events__:
* click
* doubleclick
* mouseover
* mouseout
* mousedown
* mouseup
* mousemove

__Key events__:
* keydown
* keyup

__Other events__:
* `window.onload`: when the document is loaded

__Example 1__: events.


### 3. Javascript Events

Attach or manage events for DOM elements. For example,

```
	var btn = document.getElementById("");
	var input = document.getElementById("");
	
	btn.onclick = function(){};
	input.onkeydown = function(){};
	window.onload = function(){};

	btn.addEventListener("click", function(){});
	input.addEventListener("keydown", function(){});
```

__Example 2__: events.

### 4. Practice

__Example 3__: calculator.
