# JavaScript

## Lesson 17 - Animation

### 1. Recall: 

- __Draw image on Canvas__:

```
	<img id="my_image" src="" width="" height=""/>
	
	var my_image = document.getElementById("my_image");
	
	ctx.drawImage(my_image, dx, dy);
	ctx.drawImage(my_image, dx, dy, dw, dh);
	ctx.drawImage(my_image, sx, sy, sw, sh, dx, dy, dw, dh);
```

	
- __Use image data__

```
	var imageData = ctx.getImageData(x, y, w, h)
	var imageData = ctx.createImageData(w, h)
	ctx.putImageData(imageData, x, y)
```

### 2. Animation

__Animation__ is more a dynamic drawing on canvas. To make an animation, we need a way to shedule the drawings, each drawing at a time called as a __frame__, to make them appear one by one along the time.

There are three ways to accomplish this goal:

- use Javascript function __`setInterval()`__ to schedule actions to repeat periodically, each action generates a frame.

- use Javascript function __`setTimeout()`__ to trigger the next action, drawing the next frame, after the current action, frame drawing, is done.

- use animation function __`requestAnimationFrame(callback)`__ to tell the browser that you wish to perform an animation and requests that the browser call a specified function to update an animation before the next repaint.	

In this lesseon, we will only focus on the first way, that is, using __`setInterval()`__.


### 3. `SetInterval()`

In Javascript, __`setInterval()`__ is used to shedule a series of repetitive actions. A code sample is as follows:

```
	var ms; //interval in milli-seconds
	
	function draw_frame(){ ... }
	
	setInterval(draw_frame, ms);
```

where we put the code for drawing a new frame in function `draw_frame()` and control the animation speed with a time interval value united in milli-seconds.

__Example 1__: digital clock.

	
### 4. Practice

Draw flying balls. Each ball has it's own speed and flies at a certain direction. It changes direction following the reflection law when it hits the border of the canvas. 

__Example 2__: draw a flying ball.
__Example 3__: multiple flying balls.	
	
### 5. Homework

Redo Example 2 and 3.
