# P5 OUTSIDE OF THE BROWSER
Hey everyone, this week we're going to be downloading our first IDE (Integrated Development Environment) to write code outside of the browswer. The IDE that we're going to be using for this class is called Visual Studios Code, and you can download it **[here](https://code.visualstudio.com/Download)**

These environments often have plugins for a variety of different languages, and give us more control on the assets we load in, and the workflow that we use to make our programs. Go ahead and download this softare and then come to the next step.

## Navigating the new Environment

### P5 in Visual Studios Code.
- On the left hand side your going to see a few icons, one of these icons is four small boxes, one of which is detached from the rest. If you hover your mouse over this icon it will say "Extensions". Click this.
- In the extension search bar type in "P5 Project Creator", go ahead and add this extension.
- Next type in "Live Server" and download this plugin as well.
- Download these as well( javascript es6 code snippets, p5 code snippets)

Great! At this point we pretty much have everything we need to create a p5 sketch in visual studios code. However there are now some new considerations that we have to make. For instance, before when we were coding on the web editor all of our files (index.html, sketch.js, cat.jpg, style.css... etc) were being saved online for us. Now that we're going to be using Visual Studios Code we'll have to set up the location that we want our files to be saved.

- Go ahead and create an Empty file on your desktop, name it whatever you want.
- Next navigate back to Visual Studios Code.
- On the top bracket hover over the 'file' dropdown, then click 'open folder' and navigate to your empty folder.
- On the top bracket you will see a dropdown menu labled 'view', navigate there and then press 'Command Pallete' this can also be done by pressing 'ctrl + shift + p'
- Inside your command pallete type 'create p5.js project', the plugin that we added has added this easy command here, now that we've chosen this once it will show up on the top of our command pallete in 'recently used'.
- Click this
- Name your js file whatever you want, name your html file 'index'

There you go! 
- Click on the sketch file on the side and go ahead and write some code!


### How can I use html and CSS on top of or below my sketch?
The way we have been layering things in p5 is by adding them either later or earlier in the sketch, so that they are rendered in a particular order. 
However you may want to layer HTML on top of a p5 sketch, or layer a p5 sketch on top of your html. In order to do this we're going to have to standardize the language that we use to refer to our sketch so that we can talk about it in our html file.

We can do that by naming our createCanvas instance, and then parenting that instance to an HTML 'ID'

```
 let cnv = createCanvas(windowWidth, windowHeight);
 cnv.parent('myContainer');
```
#### DIVS (html)
What this code does is it allows us to add p5 to a div that has the ID 'myContainer', then whatever we do to that div will happen to our sketch.
Next what we're going to have to do is navigate to our html and add a div that has an ID of 'myConatiner'. Lets do a quick review on divs before we do this.
A div is essentially a distinct section of our html code that we can stylize in distinct ways. You can label these divs with an Id, which is reserved for labeling individual divs, or if you want a variety of divs to use the same stylization you can use classes. 

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
<div id='myContainer'>    Anything I type here will be displayed on the page, and live in this div    </div>
<div class='funClass'>    Anything I type here will be displayed on the page, and live in this div but also its a class!    </div>                                                                
```
