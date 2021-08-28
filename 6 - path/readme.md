# JavaScript

## Lesson 6 - Path: canvas data model 

### 1. Recall: 

- Canvas API for drawing an arc:

```
    ctx.beginPath();
    ctx.arc(cx, cy, r, a1, a2, false);
    ctx.fill();
    ctx.stroke();	
```


### 2. Path

__Path__ is the data model of a shape to be rendered, either by filling or by drawing the edge (stroking). 

A path can be seen as a list (ordered) of connected or disconnected lines or curves.

Path API:

```
    //start to form a path
    ctx.beginPath();

    //methods for constructing elements of a path    
    ctx.moveTo(x,y);
    ctx.lineTo(x,y);
    ctx.arc(cx, cy, r, a1, a2, dir);
    //ctx.arcTo(x1, y1, x2, y2, r);
	
    ctx.closePath();
	
    //render the path	
    ctx.fill();
    ctx.stroke();
```

Here is the meaning of all the new APIs:

- `ctx.moveTo(x,y)`. Move the point to position (x,y) without generating an edge.
- `ctx.lineTo(x,y)`. Make a line from the current position (stored in memory) to the given position (x,y). The new position after the function call is (x,y).
- `ctx.clothPath()`. Make a line from the current position (stored in memory) to the starting position and make a enclosed shape.

### 4. Examples and Practice

__Practice 1__: [pie chart](pie_chart.htm).

__Practice 2__: [digits](digits.htm).

### 6. Homework

Write a four-component pie chart function and try some examples.

Write functions for drawing a few capital characters.

