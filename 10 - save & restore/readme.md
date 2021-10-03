# JavaScript

## Lesson 10 - Save / restore Context 

### 1. Recall: 

- __Transformation__: on the __2D coordination system__ of the canvas.

  `ctx.translate(x,y)`
  
  `ctx.rotate(alpha)`
  
  `ctx.scale(x, y)`
  
- __Context__: all the information representing a drawing state on the canvas. It includes the color chosen, the line width, the transparency level, and even the current transformation of the coordination system.   

### 2. Draw Text

- We can draw text the same way we draw a shape. The related API is:

  `ctx.fillText(text, x, y)`
  
  `ctx.strokeText(text, x, y)`

  Here, by default, `x` and `y` gives the __left-bottom corner__ of the text.

- We can also control the font of the text through `ctx.font="yyyy nnpx xxxxxxxxx"` where:
	- "yyyy" stands for the __font style__ and can be `"bold"`, `"italic"` or their combination `"bold italic"`.
    - `nn` is an integer value, standing for the __font size__.
	- "xxxxxxxxx" is the __font family name__, like "Arial", "Courier New", "Times New Roman", etc.
  
__Example__: _text_example.html_. 

### 3. Context Save / Restore:

In application we often need to reverse any changes, including the transformation on the coordination system. We can use the following API to do this job:

  `ctx.save()`
  
  `ctx.restore()`

These two functions, one for save the current context, the other for restore a previously saved context, are used in pair. The saved context instances are organized in a stack (a FILO style data structure). So, we can do multiple context saving actions, and each restoration restores the latest context instance.
 
__Example__: _flower.html_. 

### 3. Practice:

See _words_wall.html_. 
	
### 5. Homework

Draw more words in the words wall example.
	
	


