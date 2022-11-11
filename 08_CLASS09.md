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

## anchor tags
 One thing you'll notice about quite a bit of websites is that they typically have more than one page, often they have dozens. Its Impotant to know how to link to other pages while your using html. Using an *anchor tag* is how you do this.

 ```
<a>             </a>
 ```
 
 They look just like this. If you put anything between them it will display on the page in the same way it does with a div.
 However if you add this code:
 
  ```
<a href="somewebsite.com">             </a>
 ```
It will navigate to whatever webpage that you want it to. This is not only how we refer to external links, but also internal links. Everyone go ahead and create a *new* htnml file. Take a few minutes to add some nice text, stylize it if you want. 
 
Now create an anchor tag on your first html page, and link to it in your anchor tab.
 
 ```
<a href="other.html">             </a>
 ```
 Try it out, does it work?
 
 
## Inputs on HTML

### Buttons
Another thing your going to want to add to a lot of your website are dynamic buttons that are capable of doing a variety fo things. Go ahead and create a button based on the code below. You'll see the code in between the brackets gets written on the button. Go ahead and play around with stylizing it!

```
<button type="button">Click Me!</button>
```

Now this is great, but this button does absolutely nothing. Lets say we wanted to have this button update the speed of our square every time that we pushed it. We're about to dive into the wild world of event handlers so hold on! 

We won't be able to do this in just html, we're going to have to do this in javascript, in order to write javascript in a html file we'll need to add a script tag:

```
        <script>

        </script>
```
Anything that we write in here will be executed in javascript. So before we do anything lets write out in pseudocode what we're *trying* to do.
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-

```
        <script>
            function changeSpeed(){
                xSpeed += 5
            }

            let button = document.getElementById('button')
            button.addEventListener('click', changeSpeed)

        </script>
```

## (button example) [https://editor.p5js.org/dunkFig/sketches/cQdZmMuT-]

### Sliders
Sometimes we'll want to add something like a range slider to our html, that we can use to change something in our javascript or p5. 

There area variety of inputs in html and javascript, what are a few you can think of?

the way that we add a slider is by adding an 'input' tag like this, for best practices, lets also put this in its own little div.

```
<div class="slidecontainer">
  <input type="range" min="1" max="100" value="50" class="slider" id="myRange">
</div>
```
You'll see a few things here, we've specified the type, it's minimum, its max, and the value that ity'll be starting at, then we've give it a neat id. Lets go ahead and turn this element into a javascript variable as well. 

```
  
        <script>

           let sliderVal = document.getElementById('myRange').value
           slider.addEventListener("change", updateSlide)

           function updateSlide(){
                yPos = sliderVal
            }
            
        </script>

```

Lets see if this works!


##  Websites as Art, Websites as activism

- (The Apartment - Sam Levigne, Tega Brain)[https://whitney.org/artport-commissions/new-york-apartment/index.html]
- (The Yes Men - hijinks) [https://theyesmen.org/hijinks-all]

- (Her Visions) [https://www.hervisions.world/projects]
- (Control the Virus) [https://controlthevirus.art/]
- (Geo Goo)[https://geogoo.net/]
