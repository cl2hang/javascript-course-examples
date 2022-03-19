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
	
- __Use `setTimeout()`__

```
	var timeout; //in milli-seconds
	
	function draw_frame(){ 
		... 
		setTimeout(draw_frame, timeout)
	}
	
	draw_frame();
```

### 2. `requestAnimationFrame()`

__`requestAnimationFrame(callback)`__ is the 3rd way to implement an animation. It is also the recommended way to do so because it is optimized for the browser for the best performance and render.

The way to use this API is as follows:

```
	var last_timestamp = 0; //in milli-seconds
	
	function draw_frame(timestamp){
		
		//TODO: rendering 

		var elapse = timestamp - last_timestamp;
		//TODO: updating
		
		last_timestamp = timestamp;
		requestAnimationFrame(draw_frame);
	}
	
	requestAnimationFrame(draw_frame);
```

where the function `draw_frame(timestamp)` takes a parameter indicating the current time as a timestamp. The meaning of a timestamp can be seen [here](https://www.epochconverter.com/).

__Example 1__: clock.

	
### 4. Practice

Draw flying balls with a tail.

__Example 2__: draw a flying ball.	
	
### 5. Homework

Redo Example 1 and 2.
