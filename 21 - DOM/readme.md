# JavaScript

## Lesson 21 - DOM

### 1. Tree Data Structure

Just like the data structure, __queue__, we talked before. __tree__ is another type of data structure. It supports modeling hierachical structures.

See [here](https://www.geeksforgeeks.org/introduction-to-tree-data-structure/) for more detail.

### 2. HTML DOM

__DOM__ (Document Object Model) is a a tree based model of the HTML web page data in the browser. We can rely on this model as the API functions provided to work on the whole web page in Javascript.

Specifically, with DOM, JavaScript can:
* get all the power it needs to create dynamic HTML:
* change all the HTML elements in the page
* change all the HTML attributes in the page
* change all the CSS styles in the page
* remove existing HTML elements and attributes
* add new HTML elements and attributes
* react to all existing HTML events in the page
* create new HTML events in the page

In the DOM tree, each HTML element is represented as a __tree node__. The highest level node, corresponding to the __HTML__ element, is __`document`__. With this object, we can
* use __`document.body`__ to refer to the __body__ element.
* use __`document.getElementById()`__ to refer to any element in the document by giving corresponding ID.

For any current tree node (suppose it's __`n`__), we can use the following method or attribute:
* __`n.innerHTML`__ to get or modify the encluded HTML content;
* use any HTML attribute name, like __`n.style`__, to modify the corresponding HTML attribute;
* use methods like __`n.firstChild`__, __`n.nextSibling` __, __`n.parentNode`__ to navigate in the tree.
* use methods __`document.createElement()`__ to create a node correspondgin to an HTML element, and __`document.createTextNode()`__ to create a text node.
* use method __`n.appendChild()`__ to add a newly created node to the children of the current tree node.


	
### 3. Practice

__Example 1__: chatting bot.