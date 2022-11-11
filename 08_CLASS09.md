# Refining our HTML, Political Websites, Art Websites
So Today we're going to be starting off by doing a quick excercise in the p5 window, and then were going to continue to solidify some of our html knowledge.
Finally we're going to look at a few websites which exist as art and activist pieces, identify what the artists are trying achieve conceptually, and break down how they are achieveing these things technically.

## Did anyone continue building their website, check out a new library?


## First Challenge
Just to get our brains moving a little but we're going to start off by creating a p5 sketch, you can do this in either the web editor or Visual studios code, whatever works for you *we're going to be ultimately working in visual studios code today*.

- Create a rectangle that bounces around the canvas, bouncing off of its ends. 
- Make the red Value of the background dependent on the X Location of the rectangle.
- Make the blue Value of the background dependent on the Y locvation of the rectangle.
- Make the green Value of the background '0'

In order to do this you will have to map the Xpos, and Ypos from 0 - width/heigh, to 0 - 255. 
Some questions that might help jog your memory around this:
- What variable do I need to update to create motion on the x axis, y axis
- How do I adjust the speed of this rectangle (do you want to have this be it's own variable?
- How do I set conditions for allowing my shape to 'bounce' off the ends? What will I have to do to my 'speed' variable?

Go ahead and work on this, then we're going to go through it together as a class.


## Manipulating our sketch in html

Lets review how we've been bring our p5 sketches into our html arena!

The way we have been layering things in p5 is by adding them either later or earlier in the sketch, so that they are rendered in a particular order. 
However you may want to layer HTML on top of a p5 sketch, or layer a p5 sketch on top of your html. In order to do this we're going to have to standardize the language that we use to refer to our sketch so that we can talk about it in our html file.

We can do that by naming our createCanvas instance, and then parenting that instance to an HTML 'ID'

```
 let cnv = createCanvas(windowWidth, windowHeight);
 cnv.parent('myContainer');
```

Ok this is great, but if we fire off this code as is we're actually going to get an error - particularly because we have not created an html 'div' with this 'id.' Lets navigate into our html file and do this.

#### DIVS (html)

A div is essentially a section of our html code that we can stylize in distinct ways. You can label these divs with an Id, which is reserved for labeling individual divs, or if you want a to style a variety of divs you can use classes. 

```
// Below is a standard div
<div>    Anything I type here will be displayed on the page, and live in this div    </div>

```

You'll notice that there it is somewhat like our functions in that there are brackets to show the beginning and end, however they look different. The beginning of a div will look like this:

```
<div>
```

the end of a div will look like this:

```
</div>
```

anything you put between them will be text that lives inside that div. If you want to add an id or a class to your div you add it like this:

```
<div id='myContainer'>      </div>
```
Great! no we have a div that we have parented our p5 canvas to. Lets move onto stylization by referring to this in our CSS file. 



##  Websites as Art, Websites as activism

- (The Apartment - Sam Levigne, Tega Brain)[https://whitney.org/artport-commissions/new-york-apartment/index.html]
- (The Yes Men - hijinks) [https://theyesmen.org/hijinks-all]

- (Her Visions) [https://www.hervisions.world/projects]
- (Control the Virus) [https://controlthevirus.art/]
- (Geo Goo)[https://geogoo.net/]
