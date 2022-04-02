# JavaScript

## Lesson 19 - Animation

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

__`requestAnimationFrame(callback)`__ is the 3rd way to implement an animation. It is also the recommended way to do so because it is optimized for the browser for performance and appearance.

The way to use this API is as follows:

```
	var last_timestamp = 0; //in milli-seconds
	
	function draw_frame(timestamp){
		
		//TODO: rendering 

		var elapsed = timestamp - last_timestamp;
		//TODO: updating
		
		last_timestamp = timestamp;
		requestAnimationFrame(draw_frame);
	}
	
	requestAnimationFrame(draw_frame);
```

where the function `draw_frame(timestamp)` takes a parameter indicating the current time as the total time, in milliseconds, elapsed since the web page is loaded. 

__Example 1__: clock.

	
### 3. Practice

Draw flying balls with a tail.

__Example 2__: draw a flying ball.	

### 4. Javascript Object

In Javascript, __object__ is a combination of data values, each called as a __property__, and inner functions, each called as a __method__. Same as in all other languagues, we use object t model things, either real objects in the physical world, or abstract or conceptional things in our mind. 

For example, to model a car in the code, we can define an object as follows:

In grammar, an object is a composition of a list of __name/value__ pairs where the name is a label of the property or method, and the value is the current value of the property or the implementation function of the method.

```
var car = {type:"Fiat", model:"500", color:"white"};
```

```
var person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

```
var message = {
	content: "Hello World",
	display: function(){alert(this.content);}
};

message.display();
```

As shown above, to access the content of an object from outside, we use the code of formats __object_name.property_name__ or __object_name.method_name(parameters)__. If we want to access the content from inside, we use the keyword __this__ instead of the object name.

### 5. Homework

Redo Example 1 and 2.
