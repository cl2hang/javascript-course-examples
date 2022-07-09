# JavaScript

## Lesson 23 - Canvas Events (Key Events)

### 1. Recall

__HTML DOM__

* A tree based model of the HTML web page data in the browser
* Each HTML element is represented as a __tree node__. 
* The highest level node, corresponding to the __HTML__ element, is __`document`__
* use __`document.body`__ to refer to the __body__ element.
* use __`document.getElementById()`__ to refer to any element in the document by giving corresponding ID.

__HTML Events__

* Mouse events: click, doubleclick, mouseover, mouseout, mousedown, mouseup, mousemove
* Key events: keydown, keyup
* Other events: `window.onload`


### 2. Canvas and key events

Canvas is a special HTML element, most of the HTML events also apply to canvas. What's more interesting, since canvas is a space for drawing anything on it, we can use event directly on canvas to control the drawing or animation for canvas.

Here, we only focus on the key events, e.g., key up and key down. 

Firstly, any key on the keyboard has a particular code related to it. Please visit [this webpage](https://www.toptal.com/developers/keycode) to try and the code attached to each key.

In Javascript, an event object is sent to the key event handler which contains the key code. That is, suppose we have the following code:

```
function onKeyDown(e){...}

canvas.addEventListener("keydown", onKeyDown, true);
```   

where function `onKeyDown()` is registered as the key down event handler, the argument `e` is the corresponding event object. We can simply use __`e.keyCode`__ to retrieve the key code. 

__Example 1__: try key codes.

__Example 2__: moving box.


### 3. Practice

__Example 3__: spider game.

This is a simplified version of the Snake game. Different to a snake, a spider is only a dot and does not change is size. The moving direction of a spider is controlled by the arrow keys on the keyboard. A new prey is put at a random place when the spider catches one.
