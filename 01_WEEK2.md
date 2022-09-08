# Week 02 – Adding variance
* Reading Discussion
* HomeWork Discussion
* [BREAK]
* Variables
* Arithmetic (+, -, *, /, %)
* Introduction to ```random()```
* Loading Images
* [BREAK]
* More Draw Functions
* Homework Prep


## Review of what we've done so far
```
// All of our instructions are plase inside of the setup function or 'Block'
function setup() {
  createCanvas(500, 500);
  noStroke()  

  fill(255, 255, 0);
  rect(0, 0, 250, 250);
}
```

## Variables    
### What is a variable?  
  
- A way to introduce variation on a theme, generalization within a formal structure, or the abstraction of some parts of a process. The word comes from vary like variety and variance, and means a thing that is able to change.
- A variable is a placeholder. A placeholder for a value. Instead of using a specific value (like a number), you create a name, and then use that name in your code. When looking at your code, you don't know exactly what the value of that variable is. You can set it to a specific value, or change that value later. This means that one bit of code is now able to do different things.
- A variable is a way to store something in memory so you can access it later in your code.


#### _Who remembers algebra?_
  ```
  y = m * x + b aka the formula for a line
  ```

```Y``` is equal to the variable ```M``` times the variable ```X``` plus the variable ```B``` this gives us the forumla of a line where ```M``` defines the slope of the line and ```B``` define the point that the line crosses the ```Y``` axis, when ```x = 0```.

  ```
  a**2 + b**2 = c**2 aka Pythagorean Theorem
  ```

So lets talk about how you create a variable in code. The word for that is _declare_. 

This is how you _declare_ a variable in p5.js.

```
let x;
```

Before you can use a variable you have to assign it a value.

This is how you _assign_ a variable in p5.js.
```
let x; 
x = 10;

or 

let x = 10;
```

### WHERE TO DECLARE A VARIABLE?

- Inside a _function_ or a _code block_ which is called _local variables_

```
function setup()
{ 
    let x;
    print(x)
}
```

- Outside of all _functions_ which is called _global variables_
```
let x;
function setup()
{
    print(x);
}
```
### Variable Names 
* must start with a letter or an underscore character
* cannot start with a number
* can only contain alpha-numeric characters and underscores (A-Z, a-z, 0-9, and _)
* are case-sensitive (treeheight, TREEHEIGHT, TreeHeight, and treeHeight are all different variables)

### Some ways to make variables more legible?

```
camelCase
let makeItEasyToRead = 1;

snake_case
let make_it_easy_to_read = 1;

camelCase
let makeItMeanSomethingUnique = 1;

snake_case
let make_it_mean_something_unique = 1;
```

You can store multiple types of data as a variable.
- strings ```"The platypus is my favorite animal but gosh are they meanies"```
- floats ```0.01```
- integers  ```5```
- booleans ```True/False```  
- and more complex data types (we'll get to that much later on in the course)

lets look at some [code](https://editor.p5js.org/dunkFig/sketches/EObf-UgEE)


### basic math && some new ideas
* add (+)
  * 1 + 1 = 2
  * 1++ = 2
* subtract (-)
  * 1 - 1 = 0
  * 1-- = 0
* multiply (*)
  * 2*2 = 4
  * 4*4 = 16
* divide (/)
  * 2/2 = 1
  * 1 / 2 = 0.5
* pow (**)
  * 2**2 = 4
  * 3**4 = 81 
* modulus (%) 
  *  1 % 4 = 1
  *  2 % 4 = 2
  *  3 % 4 = 3
  *  4 % 4 = 0
  *  5 % 4 = 1
  *  6 % 4 = 2
  
## ```random()```
```
 let r = random(50);
 stroke(r * 5);
 line(50, height/2, 50 + r, 0);
```

One thing that works really nicely with variables is creating randomized variation of those variable values.  In p5.js, this is done with the function ```random()```. ```random()``` returns a floating point (a number with a decimal point).
Like this:
```
let firstSquareHeight = random(10,300);
```
The parameters to ```random()``` are minimum and maximum values. They define a range from which ```random()``` chooses a number. Like asking a person to "pick a number between 10 and 300".

Here is how we could use random values to draw the above composition:

```
function setup() {
  createCanvas(600, 600);
  let squareWidth = random(10,300);
  let firstSquareHeight = random(10,300);
}
```
Stop and run that a few times to see what kinds of variation we've just created.

[Random Sketch]()

## Loading Images 
```
let img;
function preload() {
  img = loadImage('/assets/PRI_220306753.webp');
}
function setup() {
  createCanvas(img.width, img.height);
  image(img, 0, 0);
}
```

### Preload

```function preload()``` is automatically called before ```function setup()```.  When you want to use images in your ```function setup()``` you must load them within ```function preload()```.

```
function preload(){

}
```

```
let img = loadImage(path)
```
- path String: Path of the image to be loaded (this must be relative to your project directory)


```loadImage(path)``` is a function that returns an image.  It must be called in ```function preload()``` and used to assign a variable if you want to use the image in the ```function setup()``` code block.

### Drawing an Image
```
image(img, x, y, [width], [height])
```
- img p5.Image|p5.Element: the image to display
- x Number: the x-coordinate of the top-left corner of the image
- y Number: the y-coordinate of the top-left corner of the image
- width Number: the width to draw the image (Optional)
- height Number: the height to draw the image (Optional)


## New Draw Functions
### arc()


```
arc(x, y, w, h, start, stop, [mode], [detail])
```

[Arc on p5 Reference Page] (https://p5js.org/reference/#/p5/arc)


## Homework
* Read Lev Manovich's [The Language of New Media, Cambridge, MA: MIT Press, 2002. Chapter 1 (pages 18-55)](https://dss-edit.com/plu/Manovich-Lev_The_Language_of_the_New_Media.pdf)
  * For the PDF Page 18 of the book is really 29
* Coding Assignment #1 __Solve LeWitt's Trapezoid__ 
![Trapezoid](images/lewitt-trapezoid.jpeg)
