# JavaScript

## Lesson 4 - _`for`_ loop (continued) 

### 1. Recall: structure of `for` loop

`for(let i = 0; i < 5; i++) {}`

`for(let i = 1; i <= 5; i++) {}`

where `i` is a __variable__, the values `0`, `1` and `5` are __constants__, and the literals `for` and `let` are __keywords__.  	

### 2. A practice

__Question__: draw squares diagnally on a 400 * 400 canvas that: (1) the adjacent squares touch each other by the top-left and bottom right cornor; (2) the width of the squares follows the pattern of 200, 100, ..., 1 where each next square has a half of the width of the current one. 

See [example_1](example_1) for the code.

### 3. use RGB color in `for` loop

We can also use `rgb()` to define a color code.  for example, each pair of the following color codes are equivalent:
- __red__: `'#ff0000'` and `rgb(255, 0, 0)`
- __green__: `'#00ff00'` and `rgb(0, 255, 0)`
- __blue__: `'#0000ff'` and `rgb(0, 0, 255)`
- __white__: `'#ffffff'` and `rgb(255, 255, 255)`
- __black__: `'#000000'` and `rgb(0, 0, 0)

__Example__: Red, green, blue and gray colors from bright to dark. See [example_2](example_2).

### 4. Double loop

We can nest `for` loops together to make multi-layered loops. The most common case is a double loop which is composed by two layer of `for` loops.

```
for(let i = 0; i < 5; i++) {
  for(let j = 0; j < 5; j++) {
    //repeated code block
  }
}
```

__Example__: [Color palette](color_palette.htm). 

### 5. Code analysis

__Discussion__: Whether to use `for` loop?

### 6. Homework

- Repeat __practice 2__ by defining a new pattern.
- Repeat __practice 4__ by using circles instead of squares and by changing the color scheme.

