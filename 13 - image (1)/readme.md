# JavaScript

## Lesson 13 - Drawing image on Canvas (1) 

### 1. Recall: 

- __HTML `<img>`__:

  `<img src="" width="" height="" alt=""/>`
  
- __image layouts__: 
  
  `display:none;`, `display:inline;`, `display:block;`
  
- __Hyperlinks, `<a>` and `<map>/<area>`__  

	`<a href="">...</a>`
	
	```
	<img src="" width="" height="" alt="" usemap="#my_map"/>
	<map name="my_map">
		<area type="rect" coords="x1,y1,x2,y2" href="" alt="">
		<area type="circle" coords="cx,cy,r" href="" alt="">
	</map>
	```
  
- __Misc__:
	
	- The Tic-tac-toe example.
	- generate random numbers: `Math.floor(Math.random() * N)`


### 2. Drawing Image on Canvas

We can load an image from an HTML `<img>` element and draw it on the canvas.

Suppose the image is defined as follows:

	`<img id="my_image" src="" width="" height=""/>`
	
Then, we can get the image object in JavaScript by:
	
	`var my_image = document.getElementById("my_image");`
	
When we have the image, we can draw it on canvas with either of the following functions:

```
	ctx.drawImage(my_image, dx, dy);
	ctx.drawImage(my_image, dx, dy, dw, dh);
	ctx.drawImage(my_image, sx, sy, sw, sh, dx, dy, dw, dh);
```
 
where, `dx`, `dy`, `dw` and `dh` together give an area on the canvas, while `sx`, `sy`, `sw` and `sh` together give an area on the image. That is, only the area on the image will be shown on the give area of the canvas.

When only `dx` and `dy` are given, the size of the canvas area is the original size of the image. When the image area is not given, the whole image should be shown.  
	

__Example 1__: redo the Tic-tac-toe example with images as the chess bits.
__Example 2__: flower wall.
	
### 3. `switch-case` Statements

It's a good chance to think about the `switch-case` clause instead of a long `if-else` statement when we have to deal with multiple choices. For example, if we want to do something if the target object is red, do some other things when it's gree,. and other actions for other colors. Just like the following:

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

For this code, the browser will check the `color_code` value and run the corresponding execution under the `case` labels until it meets a `break`. When no `break` is found, it will go through to the code in the next case block. If no case block is matched, the code under `default` will be executed. So, in this example, we have the same execution for cases 3 and 4. 
	
### 4. Practice

Following the idea of Example 2, Draw a wall of alphabets (from the given image in the "asset" folder). Use all three types of transformation while drawing.
	
