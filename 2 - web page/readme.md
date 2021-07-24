# JavaScript

## Lesson 2 - What is a web page?

### 1. How it works (more detailed)

- We explore web sites by using the __browser__ on our computer or hand-held device to retrieve __web pages__
- We can see each web site as a collection of interconnected (by __hyperlinks__) web pages, staticly stored or dynamically generated.
- Each web page has a unique address, called __URL__. A browser retrieves a web page by providing the URL.    

### 2. What's in a web page?

- A web page is a text file.
- The content of a web page normally consists three parts: (1) __HTML__ markup containing the information to be shown for user; (2) __CSS__ stylesheet controlling the rendering of the web page content; (3) __Javascript__ script makes the web page interactive. 

### 3. More Canvas API

In addition to the following Javascript statements we introduced in last lesson:

- __`ctx.fillRect(x, y, w, h);`__ 
- __`ctx.beginPath();ctx.arc(cx,cy,r,0,Math.PI*2,true);ctx.fill();`__
- __`ctx.fillStyle="...";`__
- __`ctx.globalAlpha=n.n;`__

We introduce a few more for drawing the edge of a rectangle or a circle:

- __`ctx.strokeRect(x, y, w, h);`__ drawing the edge of a rectangle with __`(x,y)`__ as the top-left corner and __`w`__, __`h`__ as the width and height.
- __`ctx.beginPath();ctx.arc(cx,cy,r,0,Math.PI*2,true);ctx.stroke();`__ drawing the edge of a circle with __`(cx,cy)`__ as the center and __`r`__ as the radius.
- __`ctx.strokeStyle="...";`__ setting the edging style (color or pattern). You can find the color code in the form of __`#xxxxxx`__ in [Google Color Picker](https://g.co/kgs/LQMmMB).
- __`ctx.lineWidth=n;`__ setting the width of the edge. __`n`__ is the number of pixels for the width.

### 4. Practice

- [Square matrix](square_matrix.htm)
- [Abstract circles](abstract-colorful-circles.htm)

### 5. Homework

- Check the source code of some web pages and identify Javascript code in each web page.
- Repeat the example code in the lesson.
- Choose some exercise pictures and implement them with the API we've learnt.