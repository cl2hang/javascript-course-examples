# JavaScript

## Lesson 7 - `if`-`else` statements 

### 1. Recall: 

- Canvas API for path:

```
    ctx.beginPath();
    ctx.moveTo(x,y);
    ctx.lineTo(x,y);
    ctx.arc(cx, cy, r, a1, a2, false);
    ctx.closePath();
    ctx.fill();
    ctx.stroke();	
```

- Canvas API for path:
	- code structures: sequential, branching, loop
	- `for` loops 

### 2. branching and `if`-`else` statements

__Branching__ is a type of code structure that the next statement to be executed is depended on a condition test. The condition test result can be of two values: __true__ and __false__.

__`if`-`else`__ statement is the most common way to implement branching. It comes with the following forms:

```
    if(boolean_expression) {
	  //do something if the boolean expression is true
    }
    //jump here if the condition is false, or come here after the if content is executed

	
	if(boolean_expression) {
	  //do something if the boolean expression is true
    } else {
	  //do something when false
	}
    //come here after the if/else content is executed
	
	if(boolean_expression) {
	  //do something
    } else if(boolean_expression) {
	  //do something
    } else {
	  //do something
    }
```	
    
We can use comparison operators, like `==`, `>`, `>=`, `<` and `<=` to make a condition by comparing two calculation results. 
We can also combine multiple conditions with logical operators like __and__(`&&`), __or__(`||`) and __not__(`!`) to form a more complex condition.  	

__Example__: draw a chess board (8 * 8 black and white grids).


### 4. Practice

System functions `Math.random()` and `Math.floor()` are used in the following practice. Here, `Math.random()` is for generating a uniformly random value in range 0 to 1. `Math.floor()` is used to bring down a decimal (for example, 17.25) to the closest integer (17 for the example). We can use these two functions to generate random numbers of the given range. 

For example, the following code generates a random number in range 0~100 each time:

`math.floor(Math.random()*100+1);`

__Practice 1__: [simulated microbes](microbes.htm).

__Practice 2__: [estimate PI value](pi.htm).

### 6. Homework

Write a four-component pie chart function and try some examples.

Write functions for drawing a few capital characters.

