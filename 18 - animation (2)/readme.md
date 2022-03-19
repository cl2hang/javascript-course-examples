# JavaScript

## Lesson 18 - Animation

### 1. Recall: 

- Ways to implement amination:

    __`setInterval()`__

    __`setTimeout()`__

    __`requestAnimationFrame(callback)`__

	
- __Use `setInterval()`__

```
	var ms; //interval in milli-seconds
	
	function draw_frame(){ ... }
	
	setInterval(draw_frame, ms);
```

### 2. `SetTimeout()`

In Javascript, __`setInterval()`__ is used to execute an action after delaying for a certain time, called __timeout__. A code sample is as follows:

```
	var timeout; //in milli-seconds
	
	function draw_frame(){ 
		... 
		setTimeout(draw_frame, timeout)
	}
	
	draw_frame();
```

where we put the code for drawing a new frame in function `draw_frame()` and trigger the action of drawing the next frame after a timing out.

__Example 1__: sticky clock.

	
### 4. Practice

Draw flying balls with a tail.

__Example 2__: draw a flying ball.	
	
### 5. Homework

Redo Example 1 and 2.
