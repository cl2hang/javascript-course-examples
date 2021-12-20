# JavaScript

## Lesson 16 - Image Processing

### 1. Recall: 

- __Draw image on Canvas__:

```
	<img id="my_image" src="" width="" height=""/>
	
	var my_image = document.getElementById("my_image");
	
	ctx.drawImage(my_image, dx, dy);
	ctx.drawImage(my_image, dx, dy, dw, dh);
	ctx.drawImage(my_image, sx, sy, sw, sh, dx, dy, dw, dh);
```

	
- __Clip and Erase__

```
	ctx.beginPath();
	...
	ctx.closePath();
	ctx.clip();
```

`ctx.clearRect(x, y, w, h)`

### 2. Image Data

Javascipt allows us to treat part of the canvas as an image and manipulate the image data. That is, we can edit each and every pixel of the canvas just like editing an image at the pixel level.


Here are the APIs we can use for this purpose:
* generate image data for a given area: `var imageData = ctx.getImageData(x, y, w, h)`
* create image data from scratch: `var imageData = ctx.createImageData(w, h)`
* draw image using the image data:  `ctx.putImageData(imageData, x, y)`

__Example 1__: duplicate drawings.

To be noted, for the security reasons, most browsers does not allow an actual picture to be copied and manipulated. So, `ctx.getImageData()` will not work if the area defined by its parameters contains an actual picture.

### 3. Understand the image data

The image data got (referred by the variable `imageData` in the above funtions) is a data object with the following properties:
* `imageData.width`: the width of the image
* `imageData.height`: the height of the image
* `imageData.data`: the pixel level data for the image

To understand `imageData.data`, we need to introduce a new basic data type in Javascript, __array__.

In Javascript, an array represents a group of data. For example, the following are some arrays defined in Javascript:

```
	var years = [2000, 2005, 2010, 2015, 2020];
	var fruits = ["apple", "orange", "watermelon"];
```

We can get the __size__ (how many items in it) of an array by the `length` property. For example, we have `years.length` as 5 and `fruits.length` as 3 in the above examples.

We can also access each item of an array using the `[]` operator. The only thing we need is an __index__ (starting from 0) to locate the item in the array.

__Example 2__: sum up integer values then set all items as the average value.

```
	var values = [1, 5, 8, 2, 10];
	
	var sum = 0;
	for(let i=0; i<values.length; i++)
		sum = sum + values[i];
		
	alert(sum);

	var average = sum / values.length;
	for(let i=0; i<values.length; i++)
		values[i] = average;
```

Now, let's go back to `imageData.data`. It is an array of length __R\*W\*4__, where __R__ stands for the height of the image (how many pixels vertically), __C__ stands for the width of the image (how many pixels horizontally). For each pixel, there are 4 values defining it, __red__ color channel, __green__ color channel, __blue__ color channel, __transparency__ (or __alpha__ channel), all in range 0~255.

In this arry, the pixel data are ordered line by line. For example, suppose the image is 100\*100 in size, then the image data array has 100\*100\*4=40000 items, each in range 0~255. For the top left pixel (x=0, y=0), it is represented by the starting 4 values, with `imageData.data[0]` as the red color, `imageData.data[1]` as green, `imageData.data[2]` as blue, and `imageData.data[3]` as transparency. For the pixel at (x=20, y=30), there are 20\*30\*4=2400 values before its data in the array. So, we can access its color and transparency using `imageData.data[i]` where `i` is from 2400 to 2403.  

__Example 3__: manipulate image data.

	
### 4. Image Processing

With the image data API, we can actually do some priliminary __image processing__ in Javascript. Image processing is an important branch in computer science. It helps us to manipulate image to analyze it content and to help us in different ways, like picture enhancement, face recognition, etc.

__Example 4__: image processing.	
	
### 5. Homework

Redo Example 3 and 4.
