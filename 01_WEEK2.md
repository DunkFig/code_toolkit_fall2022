# Week 02 – Adding variance
* Reading Discussion
* [HomeWork Discussion](https://docs.google.com/spreadsheets/d/1oE-frETSfRk5mj9mkblAWrk3HGop5uMrPbmpaRO-pC0/edit?usp=sharing)
* [Class 02 Slides](https://docs.google.com/presentation/d/1tfQpFMTpcDzoExU_2GoSqeQ-zx47dU9ys-w94Y6PCWg/edit?usp=sharing)

## Is there an Easier Way to place shapes?
YES! I promise that this last assignment was the most grueling in terms of estimating where things are on the canvas.
We will go through a variety of ways to place things on the canvas that are easier.
I will breifly show you [this](https://editor.p5js.org/dunkFig/sketches/bx7SMdlNh) code example in class, but the concepts here are something were going to explore in more depth in the next class. 


## Variables    
### What is a variable?  
  
- A way to introduce variation on a theme, generalization within a formal structure, or the abstraction of some parts of a process. The word comes from vary like variety and variance, and means a thing that is able to change.
- A variable is a placeholder. A placeholder for a value. Instead of using a specific value (like a number), you create a name, and then use that name in your code. When looking at your code, you don't know exactly what the value of that variable is. You can set it to a specific value, or change that value later. This means that one bit of code is now able to do different things.
- A variable is a way to store something in memory so you can access it later in your code.


#### _Who remembers algebra?_
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

## Different Types of Data
You can store multiple types of data as a variable.
- strings ```"The platypus is my favorite animal but gosh are they meanies"```
- floats ```0.01```
- integers  ```5```
- booleans ```True/False```  
- and more complex data types (we'll get to that much later on in the course)

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

## Variable Class Examples


### [Variable Placeholder](https://editor.p5js.org/dunkFig/sketches/CCqXpRSc3)
Let look at this basic example where we replace all of the arguments for a rectangle with variables.

### [Variables & Arithmetic](https://editor.p5js.org/dunkFig/sketches/g0zR2a5rm)
What if the variables got their values from small equations we wrote. 

### [Nested squares 1](https://editor.p5js.org/dunkFig/sketches/y7lLaozPA)
### [Nested Squares](https://editor.p5js.org/dunkFig/sketches/EObf-UgEE)
Here's a more advanced example of how we can divide, multiply, add and subtract those variables on the fly.


  
## random()

```
 let r = random(0, 255);
 stroke(r);
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


## Random Class Examples

### [Beginner Random Sketch (height & width)](https://editor.p5js.org/dunkFig/sketches/Az_-lWPpm)
Here we look at how we can assign random values to a variable and use this to deteremine the height and width of a rectangle.

### [Random Colors](https://editor.p5js.org/dunkFig/sketches/ZizLxqX50)
We can also assign random colors!

### [4 squares](https://editor.p5js.org/dunkFig/sketches/iHguO_oks)
Lets try testing out adding constraints to our randomness, can you make 4 squares appear in their own quadrants without intersecting?

### [Advanced Random (Two Quads)](https://editor.p5js.org/dunkFig/sketches/ruwHg5wMQ)
A lot of the time we will want to try and create something random that fits within certain boundaries, this example explores creating a quad that has a random shape within the boundaries of a cube. 


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

### Drawing an Image
```
image(img, x, y, [width], [height])
```
- img p5.Image|p5.Element: the image to display
- x Number: the x-coordinate of the top-left corner of the image
- y Number: the y-coordinate of the top-left corner of the image
- width Number: the width to draw the image (Optional)
- height Number: the height to draw the image (Optional)

### [Image Example](https://editor.p5js.org/dunkFig/sketches/wfPcLSoxi)

## New Draw Functions
### arc()


```
arc(x, y, w, h, start, stop, [mode], [detail])
```

### [Arc on p5 Reference Page](https://p5js.org/reference/#/p5/arc)


## Homework
• Take the code you worked on for your last assignment or create a new picture.
• Change a variety of the parameters that your using to designate shape and placement and turn them into variables. 
• Base these sizes on 'height' and 'width' so even if you change the canvas size your image will appear in relative size to the canvas. 
• Add some randomness into your image so that everytime you refresh the page your cat looks slightly different.
