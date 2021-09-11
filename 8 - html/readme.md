# JavaScript

## Lesson 8 - HTML 

### 1. Recall: 

- branch and `if`-`else`

```
    if(boolean_expression) {}
    else if(boolean_expression) {}
    else {}
```	

- boolean values: __true__, __false__.
- mathimatical comparison: `==`, `!=`, `>`, `>=`, `<` and `<=` 
- logical operators: __and__(`&&`), __or__(`||`) and __not__(`!`)  	

### 2. HTML

- __hieriarchical__ structure of information (part-whole relationship): organization of human body, structure of a noval, etc.

- __markup language__:
	- __literal__: a string without space in between
	- __elements__: the component of a structural information. A literal embedded with `<`, `\<`, `>`, `\>`.
	- __attribute__: property of an element, in form of `name="value"`.

	Example (XML):
	
```
    <family name="Simons">
        <member type="father" name="Massimo"/>
        <member type="mother" name="Gemma"/>
        <member type="son" name="Sandro"/>
        <member type="daughter" name="Rosa"/>
    </family>
```

- HTML (__Hyper-Text Markup Language__): the markup language to form a web page.

### 3. HTML Structure

- __`<html>`__: the root node representing an HTML document
	- __`<body onload="">`__: the renderable content of the web page
		- __`<h1>`__, __`<h2>`__, __`<h3>`__, etc: section titles
		- __`<p>`__: a paragraph
		- __`<table border="1">`__: a data table, also used for layout control
			- __`<tr>`__: a table line
				- __`<tr colspan="1" rowspan="1">`__: a table cell
		- __`<button onclick="">`__: a button
	- __`<head>`__: containing the information of the HTML document
		- __`<title>`__: the caption of the page
		- __`<script>`__: the place holding JavaScript code
		- __`<style>`__: the place holding CSS definition		


### 4. Practice: tic-tac-toe

__Requirements__:
- Use `<table>` element for layout control
- HTML elements: a canvas of 500*400. Below the canvas, 9 buttons on each side for putting the chess at the given position.
- JavaScript functions are:
	- draw the board: `function draw_board(){...}`
	- draw a chess: `function draw_chess(r, c, is_cross){...}`
	- draw a cross chess: `function draw_cross(cx, cy){...}`
	- draw a circular chess: `function draw_circle(cx, cy){...}`
	- drawing context is share by these functions and initialized when the HTML page is loaded.
	
### 5. Homework

- Repeat the practice.
- Learn more HTML elements and their attributes.
	
	


