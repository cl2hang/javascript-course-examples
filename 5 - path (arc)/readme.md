# JavaScript

## Lesson 5 - Path: canvas data model 

### 1. Recall: 

- `for` loop:

```
    for(let i = 0; i < 5; i++) {}
    for(let i = 1; i <= 5; i++) {}
``` 

- Representing a color: `'#rrggbb'` or `'rgb(r,g,b)'`
- Canvas API:

```
    //draw rectangle
    ctx.fillRect(x,y,w,h);
    ctx.strokeRect(x,y,w,h);
	
    //draw circle	
    ctx.beginPath();
    ctx.arc(cx, cy, r, 0, Math.PI*2, true);
    ctx.fill();
    ctx.stroke();	
	
    //context parameters	
    ctx.fillStyle = '#ff0000';
    ctx.strokeStyle = 'rgb(255,0,0)';
    ctx.globalAlpha = 0.1;
    ctx.lineWidth = 10;
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
    ctx.arcTo(x1, y1, x2, y2, r);
	
    ctx.closePath();
	
    //render the path	
    ctx.fill();
    ctx.stroke();
```

### 3. back to `ctx.arc()` 

__Arc__ is a part of a circle. It is identified by: (1) the center and radius of the circle; (2) the start angle and the stop angle.

The __angle__ for an arc can be in __degree__ (normally 0° to 360°) or in radian mode (0 to `2*Math.PI`). That is, A circle is an arc with starting angle as 0° (or 0 in radian) and stop angle as 360° (`2*Math.PI` in radian); a half circle can be an arc with starting angle as 0° (or 0 in radian) and stop angle as 180° (`Math.PI` in radian) 

The method: `ctx.arc(cx, cy, r, a1, a2, dir)` where
- `cx`, `cy` and `r` defines the center and radius of the circle that contains the arc;
- `a1` and `a2` are the start angle and the stop angle for the arc. Both are in radian mode.
- `dir` defines the direction of the arc, `true` as conterclockwise and `false` as clockwise. 

__Example__: Draw an arc, change the value of parameters and see the effect [example_1](example_1.htm).

### 4. Practice

__Practice 1__: [nest](nest.htm).
__Practice 2__: [color wheel](color-wheel.htm).

### 6. Homework

Repeat the practices.

