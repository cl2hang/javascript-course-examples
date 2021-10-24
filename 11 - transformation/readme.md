# JavaScript

## Lesson 11 - Transformation (project) 

### 1. Recall: 

- __Transformation__: on the __2D coordination system__ of the canvas.

  `ctx.translate(x,y)`
  
  `ctx.rotate(alpha)`
  
  `ctx.scale(x, y)`
  
- Draw Text:

  `ctx.fillText(text, x, y)`
  
  `ctx.strokeText(text, x, y)`

- __Context Save / Restore__

  `ctx.save()`
  
  `ctx.restore()`


### 2. Project: clock
	
- __Requirement__: draw an analog clock.

- __Template__:

```
<!DOCTYPE html>

<html>

<head>
	<title>Clock</title>
	<script>
	
	var ctx;
	
	function draw_clock(hh, mm, ss){
		//TODO: your code goes here
	}

	
	function start(){
	
		ctx = document.getElementById("my_canvas").getContext("2d");
		
		window.setInterval(function() {
			var now = new Date();
			draw_clock(now.getHours(), now.getMinutes(), now.getSeconds());
		}, 1000);
	}
		
	</script>
</head>

<body onload="start()">
	<canvas id="my_canvas" width="400" height="400" style="border:solid black 1px;"></canvas>
</body>

</html>
```

	
### 5. Homework

Find a picture of a guage, such as a thermometer or a speed meter for cars, and draw it with JavaScript canvas.
	
	


