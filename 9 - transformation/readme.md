# JavaScript

## Lesson 9 - Transformation (1) 

### 1. Recall: 

- __HTML__ (Hyper-Text Markup Language): a tyle of __markup__ language representing the __hieriarchical__ structure of a web page.
- HTML __elements__ (forming the hieriarchical structure) and __attributes__ (describing the properties of an element)
- HTML __head__ (information about the web page) and __body__ (renderable content in the web page)
- Drawing a __table__ using HTML: elements like `<table>`, `<tr>` and `<td>`, using attributes `colspan` and `rowspan` to span a cell across columns or rows.
  	

### 2. Transformation

__Transformation__ is a way to control the 2-D coordination system for a canvas. The original __coordination system__ has (0,0) as the __center__, the __X Axis__ pointing to the right and the __Y Axis__ pointing downward.

There are 3 basic ways of transformation:
- __translate__ move the coordination on the canvas, as a result only the coordination center changes.

  `ctx.translate(x,y)`: move the coordination center `x` pixels to the right and `y` pixels downward. `x` and `y` can be negative, meaning a counter direction.

- __rotate__ let coordination spin a certain degree from the current pose but keeps the center unchanged. 

  `ctx.rotate(alpha)`: rotate the coordination of the angle `alpha` (in radian) clockwise. The effect will be counter-clockwise if `alpha` is below 0.

- __scale__ zooms the coordination to a certain ratio without changing the center poisition and the pose. The effect is like zoom in and zoom out along one or both axises.

  `ctx.scale(x, y)`: zoom ratio `x` along X-axis and `y` along Y-axix. `0<x, y<1.0` means zoom out, `x, y>1.0` means zoom in.    
  
__Example__: see _examples.html_ for the effects 


### 3. Practice:

See the examples _translate.html_,  _rotate.html_ and  _scale.html_. 
	
### 5. Homework

Repeat the practice.
	
	


