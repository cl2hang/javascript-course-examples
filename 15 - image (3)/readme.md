# JavaScript

## Lesson 15 - Mix images with shapes (2)

### 1. Recall: 

- __Draw image on Canvas__:

```
	<img id="my_image" src="" width="" height=""/>
	
	var my_image = document.getElementById("my_image");
	
	ctx.drawImage(my_image, dx, dy);
	ctx.drawImage(my_image, dx, dy, dw, dh);
	ctx.drawImage(my_image, sx, sy, sw, sh, dx, dy, dw, dh);
```

	
- __`switch-case`__

```
		int color_code;  // 0-red, 1-green, 2-blue, 3- ...

		...

		switch(color_code) {
			case 0:
				...
				break;
			case 1:
				...
				break;
			case 2:
				...
				break;
			case 3:
			case 4:
				...
				break;
			default:
				...
		}
``` 

### 2. Mix image with shapes

Besides treating images as shapes, we can also use path to form a __mask__ area, so that only the images, as well as other shapes, in this area is shown and the rest is masked.

The API used is as:

```
	ctx.beginPath();
	...
	ctx.closePath();
	ctx.clip();
```

__Example 1__: draw stars.	
	
### 3. Clear drawings

Sometimes, we want to clear some area before redrawing. To do this, we can use the following API to clear a rectangular area.

`ctx.clearRect(x, y, w, h)`

__Example 2__: small image holes.	
	
### 4. Practice

Continue with the plotting example in the previous lesson.

### 5. Homework

Redo Example 1 and 2.
