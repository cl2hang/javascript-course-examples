# JavaScript

## Lesson 20 - Course Project (Animation)

### 1. Recall: 

- __Use `requestAnimationFrame()`__



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

* __Javascript Object__

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
	
### 3. Praject

Draw flying balls with tails. Use object to model each ball.