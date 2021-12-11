# JavaScript

## Lesson 14 - Mix images with shapes (1)

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

In Javascrip canvas, an image is almost no different to a shape, except that the information contained in a image is much richer. Therefore, we can do all the operations, like transformation on image just as we do on a shape. Of course, we can also mix images and shapes together in your drawing.

Here are two examples:

__Example 1__: draw alphabets.

This example is similar to the example in the previous lesson, except that we use different transformation on images. In this way, some characters look bigger, all appear at different locations and tilted in some way.

__Example 2__: form square wave using Sine waves.

This example uses an images with other shapes together. It also shows a way in electronics for forming a square wave with Sine waves.

In specific, the formula for this purpose is:

S(t) = k * (sin(t) + sin(3t)/3 + sin(5t)/5 + ... )
	
	
### 3. Practice

Redo Example 1, adding more characters.
