# __CODE TOOLKIT FALL 2022__Week One

 - [Our Syllabus](https://github.com/DunkFig/code_toolkit_fall2022/blob/main/Syllabus.md)
 - [Resources / Inspiration](https://github.com/DunkFig/code_toolkit_fall2022/blob/main/Resources_Inspiration)
 - [Class 01 Shared Doc]()

## Introduction
### Background, context, and goals
At its core, the objective of this class is to teach you how to create software, and in the process to uncover how an embodied, hands-on practice creating software affords you new insights into how software operates unto itself, and how it interfaces with the world by shaping and mediating other social and cultural activities.

Hopefully in some of your other classes at The New School, you've had the opportunity to study critical perspectives on what software & digital machinery have wrought in the world: how they mediate so many social, cultural, political and economic aspects of life today. In this class, we will augment these critical perspectives by emphasizing production work to learn first-hand what software does, how it operates, and how it makes us think. By learning how to develop software yourself through the practice of computer programming, you will gain an intimate understanding of the core building blocks that comprise nearly all software in use today.

There are some programming techniques that you will learn in this class that won't be directly applicable to all of your future coding work (like specific programming language syntax), but hopefully everything that you learn will be applicable to future work in the sense that you will be learning the core constructs of computer programming in a foundational sense. Later on when working with other technical production tools, you should be able to recognize these core constructs such as: if statements, loops, arrays, and fundamental concepts of computation like variability and repetition.

In learning how to create computer programs, you will experience the thought processes and ideologies that come with software thinking — we might say, software epistemology. You will experience what it is like to discipline your mind into thinking like a computer programmer, which, oddly, also entails disciplining your mind into "thinking" like a computer — although whether we can call what computers do thinking is the subject of deep, long-standing, political, and philosophical debate. Understanding these core building blocks of computer programs then is a way of seeing how a world mediated by software appears, or more metaphorically, we might say: how computers see the world.

In a world that seems everywhere mediated by software, these skills are valuable in their own right. But beyond the utility or "marketable skills" of this practice, hopefully you will gain hands-on knowledge that you can bring back to other critical studies of the social, cultural, and political aspects of computer programs.

### So ... what is a computer program?
Its kind of like a recipe, where the computer is the chef.

A program is a file, like a text or .doc file. (What is a file?) It lives on your computer's disk, it consists of a series of instructions, and its formatted in a precise, special way so that your computer can read and execute the instructions listed in the file.
So when we say for example that a program is "big", it just means it consists of more instructions, so its a larger file.
What are some computer programs?
- Microsoft Word
- Adobe Photoshop
- Adobe Illustrator
- Firefox
- your favorite game

So what is computer programming?
The art or science of writing specific computer instructions for a specific task
Often called just "programming", or "coding"
Programming is a kind of translation. From the intuitive and informal way that humans communicate to each other, into a formal and very specific type of writing. This often entails describing the task in a very structured way in English, and then translating that description into a computer programming language.
Another word for this is algorithm. An algorithm is a formal process or a sequence of instructions. (Anyone know where this word comes from?) Think of some examples:
long multiplication or division
drawing a shape
sorting a deck of cards
 
Let's write a simple "program":
### How to make a drawing
There were some things that many of your drawing instructions did that we will see again later:
- placeholders: things like "the first square", "the bottom line". In computer programs these are called variables
- repetition: "do this 4 times", "do this until you connect back to the first line". In computer programs these are called loops
- questions or conditions: "if the shape is not closed, keep drawing". In computer programs these are called conditionals
- groups of commands: "draw another shape like you did in steps 1-4". In computer programs these are called functions and they are a way to make a group of instructions with a name for re-use

### Let's make a very simple example:
```
function setup(){
stroke(0,0,255)
fill(0,255,0)
rect(50,50,200,200)
}
```
[Lets Look at this in the Editor](https://editor.p5js.org/dunkFig/sketches/TaRUMIeJC)

- In p5.js, we mainly draw using coordinates. Keep in mind a grid where the top-left corner is 0,0. 
- The horizontal dimension is always specified first and is referred to as x, and the vertical dimension is always specified second and is referred to as y.
- x increases as you move to the right, and y increases as you move down.

![grid-10-10](https://user-images.githubusercontent.com/111362862/185502020-3e5e7e2c-631e-492e-9ea1-6a47747d2178.png)

So in the following example, what are the coordinates of this pixel?

![grid-10-10-pixel](https://user-images.githubusercontent.com/111362862/185502428-e9b21e8e-ba75-404f-a848-1c4aa678bc16.png)

Highlight this text for an answer: x=2, y=3. Remember, we start counting from 0.
What about in this example: what are the coordinates of this pixel?

Please don't actually count all those pixels! Let's just approximate. Maybe, x=30 and y=15? That seems about right.
Computers require us to be precise. But we can comply with that precision while also being loose and approximate in achieving the goals that we're working toward. We can leave space to play, experiment, estimate, and work by trial-and-error.

Let's look at one command in the reference: rect().
The numbers in parenthesis are called parameters and their order is very important. The reference will tell you what the various parameters do. In this case, the reference explains that the first parameter is the "x-coordinate of the rectangle", the second parameter specifies the y coordinate, the third is the width of the shape, and the fourth is the height.

Color is specified using red, green and blue components, called RGB color. Tools > Color Selector gives you a helpful tool for selecting colors.
You can also use hue, saturation and brightness, called HSB color, if you specify that with the colorMode() command. Let's modify the above example:

(Changed code will always be in orange with a thin dashed underline.)
size(300,300)
stroke(0,0,255)
fill(150,150,255)
rect(50,50,200,200)
You can always add a fourth argument to any color commands to specify alpha which is a common digital media term that means transparency: how see-through a digital image is.
(New code will always be in blue with a dotted underline.)
size(300,300)
stroke(0,0,255)
fill(150,150,255,50)
rect(50,50,200,200)
That might not seem very different but if we add a new shape it should be more apparent:
size(300,300)
stroke(0,0,255)
fill(150,150,255,50)
rect(50,50,200,200)
ellipse(250,250,50,50)
Notice that the overlap is slightly darker.
Drawing order is also important. Intructions are followed from top down, first things first. Lower commands are run later. This means that later drawn shapes will be drawn as if layerd on top of earlier ones. So it's like making a collage: the things that you place down later will be on top.
Let's add a third shape and remove the transparency to see what I mean:

size(300,300)
stroke(0,0,255)
fill(150,150,255,255) # 255 as alpha is equivalent to totally opaque
rect(50,50,200,200)
ellipse(250,250,50,50)
triangle(250,250,250,300,300,250)
Some syntax rules
Parenthesis must always come in pairs, open and closed: ( )
Processing will try to help you with text highlighting and helpful error messages. If you are confused, check the reference for relevant examples.
Comments are also an important part of coding. They are how you communicate with others (and with yourself in the future!) about what your code does. There are two ways to add comments in Python:
# Using a hashtag symbol creates a single line comment, like this
Single-line comments can also start midway through a line
rect(10,10,10,10)  # like this
"""
  Using three quotation marks, you can create a comment for a block of
  text, like this. Use this at the top of your files to include your
  name, date, and what this code is for (such as homework week number
  or project)
"""
Some comments on lecture note format & style
Throughout all my lecture notes this semester, I will indicate Processing code by highlighting it in light blue and using a fixed-width font, like so:
rect(250,250,100,50)
Whenever text is formatted in this way, it is valid Python Processing syntax. You should be able to copy/paste it into your PDE. I will try my best to also use this formatting when specifying code in my emails, but I can't promise total consistency there as that can get quite tedious.
When my notes are working through an example by making incremental changes, I will help you spot these changes: modified code will always be in orange with a thin dashed underline and new code will always be in blue with a dotted underline.
In prose text (normal, non-code writing) I will use a bold typeface to indicate special keywords that will form the basis of our shared, technical discourse this semester. I advise you to carefully commit these to memory (perhaps consider using flashcards or whatever works for you). Use them when speaking about code with me, with your classmates, and with others. Cultivating a fluency with this technical jargon is as much a part of becoming a programmer as learning programming language syntax. (I will also use italics merely for emphasis.)
A note on accessibility: I have tried to make these formatting rules as accessible as possible to everyone with all types of seeing abilities. If you have trouble distinguishing these formats for any reason, please let me know and I'd be happy to work with you to make sure they are easily discernible.
Raster images
Raster Images. You don't need to always create drawings in this way. You can also load "raster" images into your sketch, and draw them directly into the window. If you've ever done any HTML, this is similar to the way images are included in web pages.
Go to Sketch > Add File, then browse to the image file you want to add and click "Open" . This adds the image file to your sketch directory but does not actually draw it.
To draw it, use the following code:
img = loadImage("YOUR-IMAGE-FILENAME.jpg")
image(img, 0, 0)
The 0, 0 specifies the x and y location of where in the window to place the image. If you want to control the size of the image, modify the 2nd line to look like this:
image(img, 0, 0, 50, 25)
In this case, the image would be 50 pixels wide and 25 pixels tall.
Those numbers are arbitrary and just as a demonstration. You can change them or experiment as much as you'd like. You can find more information in the reference: PImage, loadImage(), and image().
Drawing like this seems tedious! Why would you ever want to do this?
When you want to create something interactive, ie, something that responds to user input. Or when you want to create something with an inhuman amount of repetition. Or maybe when you want to process a large amount of data.
Really, any time you want to create something dynamic ... Tools like Photoshop, Illustrator, and Final Cut are fantastic, but they create fixed, closed works. With programming you can produce a creation and imbue it with life.
Maybe instead of drawing an illustration, you define rules to create that illustration, and you write a computer program to draw it. Then you can introduce variance or randomness into the system and instead of 1 drawing, now you have an entire world of drawings that are all similar but also different.
Some programs are fun or helpful to use, some are tools that allow you to create things. When you are creating the program, you can create tools that allow other people to be creative.
  

## __5-10 min break__

## Our Set Up:
- We will be using the [P5.js web editor](https://editor.p5js.org/) to code and share our 'sketches'.
- [Here](https://p5js.org/reference/) is the P5.js reference page. Please bookmark this page you'll probably be opening it a lot.

___If I am ever going to fast or you have any questions please interrupt me and ask a question___


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
* [MOCK HOMEWORK EXAMPLE](https://docs.google.com/document/d/1Etdai-04MDy5KyH65QThOP9h9gtS8VfgzLv2AEY1ywU/edit?usp=sharing)

## Week 01 Homework
* Read Chapter 1 (pages 18-55) of [The Language of New Media](https://dss-edit.com/plu/Manovich-Lev_The_Language_of_the_New_Media.pdf) by Lev Manovich.
* Write a response (250-300 words)
* Create an image with p5.js that uses at least one:
    - [Ellipse](https://p5js.org/reference/#/p5/ellipse)
    - [Triangle](https://p5js.org/reference/#/p5/triangle)
    - [Quadrangle](https://p5js.org/reference/#/p5/quad) 
    - [Rectangle](https://p5js.org/reference/#/p5/rect) with curved corners.
    - Each shape should be a different color.

* _Extra Credit Readings & Watching_ 
  * The Critical Engineering Working Group's [THE CRITICAL ENGINEERING MANIFESTO](https://criticalengineering.org) [pdf](https://criticalengineering.org/ce.pdf)
  * Watch Zach Lieberman's talk at EYE0 2012 * https://vimeo.com/47203759?t=38m22s
  * Read Casey Reas et al. [{Sofrware} Structures](https://artport.whitney.org/commissions/softwarestructures/text.html#structure)
  * Check out 2 [examples](https://p5js.org/examples/)

