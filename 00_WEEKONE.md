# __CODE TOOLKIT FALL 2022__
# Week One

## Descriptive Drawing Excercise

## [Our Syllabus](https://github.com/DunkFig/code_toolkit_fall2022/blob/main/Syllabus.md)

## One on One
I want to schedule Virtual 1:Ones with everyone in the class periodically throughout the semester.  These informal chats will help me gage progress, help with confusion, and help me get to know each of you a bit better. 

## Office Hours
SCHEDULE OFFICE HOURS [HERE](https://calendar.app.google/ijii6sYBHRwy6xMv7) FRIDAY 12:00PM - 2:00PM. (If none of these times work just email me and we'll find another time :) )

## Slack
I invited you all to our slack and to our channel.  If I have missed anyone please let me know right now!  Please sign up as it is a way to contact me directly about issues with homework or readings. 

## Examples / Inspiration


## __5-10 min break__

## Our Set Up:
- We will be using the [P5.js web editor](https://editor.p5js.org/) to code and share our 'sketches'.
- [Here](https://p5js.org/reference/) is the P5.js reference page. Please bookmark this page you'll probably be opening it a lot.


___If I am ever going to fast or you have any questions please interrupt me and ask a question___


## [Hello World](   )

With p5js we start with:
```
function setup(){
  print("Hello World");
}
```
This is the traditional first program you write as a programmer. 

A ```function``` is a thing we will get into later.  But for now just know that the ```function setup()``` gets automatically called by the p5js library when the page finishes loading and eveything within the ```{}``` code block get executed. 

Inside the code block we call the ```print(string)``` function and pass in the string "Hello World".  This prints ```Hello World``` to the console. 

So to review
* ```function setup()``` gets called to start our program
* Eveything within the ```{}``` code block get executed 
* We can call ```functions``` from p5js such as 
  * ```print(string)``` to print something to the console 
  * Lets look at more of those ```functions```

## Drawing with numbers

- [Hello Shapes](https://editor.p5js.org/danzeeeman/sketches/l21Ut52K6)

Lets break down what's going on here:
```
// Setup gets called to kick off the program
function setup() {
  // Before we can start drawing we need to create the canvas 
  createCanvas(512, 512);
  // we can make it the window width and height by doing this
  // createCanvas(windowWidth, windowHeight);
  // we set a background color;
  background(255);
  //lets comment this out and see what happens
  //we turn off ugly stroke outlines
  noStroke()
  
  // Drawing a rectangle
  // we set the fill the magenta with some alpha 
  fill(255, 0, 255, 127);
  // we call the fill function and we set the fill color to magenta with some alpha 
  rect(40, 120, 120, 40);
  
  // Drawing an ellipse
  // we call the fill function and we set the fill color to yellow with some alpha 
  fill(255, 255, 0, 127);
  // we call the ellipse function and draw a ellipse which in this case is a circle because the sides are equal. 
  ellipse(50, 50, 80, 80);
  
  // Drawing a triangle
  // we call the fill function and we set the fill color to magenta with some alpha 
  fill(255, 0, 255, 127);
  // we call the triangle function and draw a triangle
  triangle(300, 100, 320, 100, 310, 80);
}
```

Lets look at the functions we use to draw shapes


```rect(x, y, width, height)```
```
createCanvas(512, 512);
fill(255, 0, 255);
rect(0, 0, 512, 512);
```

```ellipse(x, y, width, height)```
```
createCanvas(512, 512);
fill(255, 0, 255);
ellipse(0, 0, 512, 512);
```

```triangle(x1, y1, x2, y2, x3, y3)```
```
createCanvas(512, 512);
fill(255, 0, 255);
triangle(0, 0, 256, 512, 512, 0);
```

Let's look at this ```fill``` function that we keep calling.  Fill sets the fill color for our shapes.

```fill(r, g, b)```

```
fill(255, 0, 255);
```

```stroke(r, g, b)```
```
stroke(255, 255, 0);
```

```
function setup(){
  createCanvas(512, 512)
  fill(255, 0, 255);
  stroke(255, 255, 0);
  rect(0, 0, 256, 256);
  rect(256, 256, 256, 256);

  fill(255, 255, 0);
  stroke(255, 0, 255);
  rect(0, 256, 256, 256);
  rect(256, 0, 256, 256);
}
```

## The Screen is a Grid
- [Hello Grid](https://editor.p5js.org/danzeeeman/sketches/aiCnAxqRZ)
![Images](images/grid.png)

```
function setup(){
  createCanvas(512, 512);
  fill(255, 255, 0);
  stroke(255, 0, 255);
  rect(0, 0, 512, 512);
}
```

```
function setup(){
  createCanvas(512, 512);
  fill(255, 255, 0);
  stroke(255, 0, 255);
  rect(100, 100, 200, 200);
}
```

```
function setup(){
  createCanvas(512, 512);
  fill(255, 255, 0);
  stroke(255, 0, 255);
  rect(0, 0, 100, 100);
  rect(100, 0, 100, 100);
}
```

```
function setup(){
  createCanvas(500, 500);
  noStroke()  

  fill(255, 255, 0);
  rect(0, 0, 250, 250);
  
  fill(255, 0, 255);
  rect(250, 0, 250, 250);
  
  fill(255, 255, 0);
  rect(250, 250, 250, 250);
  
  fill(255, 0, 255);
  rect(0, 250, 250, 250);
}
```


# Home Work
## How to submit:
* Create a Google Doc
* Label it (FirstName_Week_#)
* If Working on code, use the [P5.js Web Editor](https://editor.p5js.org/)
* For any code that you work on, link it on the google doc with a small annotation. (Example: Self Portrait, using primitive shapes)
* You should respond to the readings on this doc as well. 
* Copy a link to your google doc into the [HOMEWORK ROSTER](https://docs.google.com/spreadsheets/d/1oE-frETSfRk5mj9mkblAWrk3HGop5uMrPbmpaRO-pC0/edit?usp=sharing)
* Homework is due midnight the night before class.
* For certain Assignments I'll ask you to email me directly.

## Week 01 Homework
* Read Marshall McLuhan's [The Medium is the Message](pdfs/mcluhan.mediummessage.pdf)
* Create an image with p5.js that uses at least one:
    - [Ellipse](https://p5js.org/reference/#/p5/ellipse)
    - [Triangle](https://p5js.org/reference/#/p5/triangle)
    - [Quadrangle](https://p5js.org/reference/#/p5/quad) 
    - [Rectangle](https://p5js.org/reference/#/p5/rect) with curved corners.
    - Have fun and play with different colors!


* _Extra Credit Readings & Watching_ 
  * The Critical Engineering Working Group's [THE CRITICAL ENGINEERING MANIFESTO](https://criticalengineering.org) [pdf](https://criticalengineering.org/ce.pdf)
  * Watch Zach Lieberman's talk at EYE0 2012 * https://vimeo.com/47203759?t=38m22s
  * Read Casey Reas et al. [{Sofrware} Structures](https://artport.whitney.org/commissions/softwarestructures/text.html#structure)
  * Check out 2 [examples](https://p5js.org/examples/)

