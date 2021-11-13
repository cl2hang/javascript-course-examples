# JavaScript

## Lesson 12 - HTML `<img>` 

### 1. Recall: 

- __Drawing basic shapes__:

  `ctx.fillRect(x, y, w, h)` / `ctx.strokeRect(x, y, w, h)`
  
  `ctx.beginPath()` / `ctx.closePath()`
    
  `ctx.moveTo(x, y)` / `ctx.lineTo(x, y)`
  
  `ctx.arc(cx, cy, r, angle_1, angle_2, dir)`
  
- __Context properties__:

  `ctx.fillStyle`, `ctx.strokeStyle`, `ctx.lineWidth`, `ctx.globalAlpha`.  

- __Transformation__: on the __2D coordination system__ of the canvas.

  `ctx.translate(x,y)`
  
  `ctx.rotate(alpha)`
  
  `ctx.scale(x, y)`
  
- __Draw Text__:

  `ctx.fillText(text, x, y)`
  
  `ctx.strokeText(text, x, y)`

- __Context Save / Restore__

  `ctx.save()`
  
  `ctx.restore()`


### 2. HTML `<img>`
	
Usage: showing image in a web page.

The grammar:
	
  `<img src='...' width='...' height='...' alt='...'/>`

Here, the meaning of all these attributes are:

- `src`: the origin of the page, such as the path to a local file, or a URL to an online resource.
- `width`/`height`: the dimension (in pixels) of the image. Default as the actual dimension
- `alt`: an extra text information explaining the image, shown when the image cannot be loaded

__Example__: manipulate images in HTML [seasons.html]().  
  
__Comments__:
- Image files come with different extension names, such as __bmp__, __jpg__, __png__ and __gif__. The extension name determines how the image data is archived in the file. Higher the compressing rate, smaller the file size given the similar quality.
- __GIF__ image is a special type of images. Not like other types of images which are all static, this type of images contain animations and are dynamic.
- Local file paths in `src` can be an absolute path, like "C\user\me\pictures\sample.jpg" or a relative path from the webpage, such as "asset\sample.jpg".
- URLs indicates that the image comes from the Internet. It is often an __HTTP(s)__ address.

__Example__: [misc.html]().

### 3. HTML `<a>`

One HTML element that often used with `<img>` is `<a href='...'/>` which stands for a __hyperlink__. With hyperlink, web pages all over the Internet are basically connected, forming a gigantic __World-wide Web (WWW)__.

The attribute `href` gives the hyperlink target as a URL of the target webpage (or other Internet element that is addressable, like an email address). 

The content of `<a>` is normally a string of text, an image, or a mix of both.

__Example__: [hyperlink.html]().  

### 4. Map Area

One even more complex hyperlink related to `<img>` is __Map Area__. The purpose is to locate certain area in an image to be a source of hyperlink.

The following is an example:

```
<img src="asset/workplace.jpg" alt="Workplace" usemap="#workmap" width="400" height="379">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Mercury" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Cup of coffee" href="coffee.htm">
</map>
```

Here, the image and the area list is connected by the id-like literal "#workmap". We can define a rectangular, circular, or even polygon, shape inside the image to be an area. To define a rectangle, the top-left and bottom-right coordination in the image should be provided. To define a circular area, the center and radius are needed.

	
### 5. Practice

[solar_system.html]().
	
