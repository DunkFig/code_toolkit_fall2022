
# CLASS 07 (Lists and our own functions)
### Lets start off with some current events:
- [Imageine Science Film Festival](https://www.imaginesciencefilms.org//ny15?gclid=CjwKCAjw7p6aBhBiEiwA83fGulcNFUchqNbW6FPrgzE2usZlyxqFJf1FwMwvCMbMJbRuPSmSmGyhMRoCI0kQAvD_BwE)
- [Mezzanine Play Through at the New Museum](https://www.newmuseum.org/exhibitions/view/first-look-mezzanine)
- [My Deep Fake Dad](https://www.culturehub.org/events/my-deepfake-dad)

### HOMEWORK
[HomeWork Roster](https://docs.google.com/spreadsheets/d/1oE-frETSfRk5mj9mkblAWrk3HGop5uMrPbmpaRO-pC0/edit#gid=0)

### MIDTERM IDEAS


### Review of Last week 
- Millis()
- State

### Refering to many things!
Today we're going to finally be getting in to storing information which we can later refer to in our sketches. There are many ways and systems that we can use to store information, the array being the simplest way. First lets take a look at a few examples thhat use lists to refer to tons of variable and shapes at the same time. 
- [Flocking 2D](https://www.youtube.com/watch?v=tOv8JGA2-mM)
- [Flocking 3D (Gene Kogan)](https://vimeo.com/39517129)

## HIP HIP ARRAY
Today We're going to begin to play around with some of these ideas by using arrays, so lets start off with an example that we're somewhat familiar with:

```

function setup(){
    createCanvas(400, 400)
}

function draw(){
   background(255)
   rect(100, 250, 100, 100)
   rect(200, 250, 100, 100)
   rect(300, 250, 100, 100)
   rect(400, 250, 100, 100)

}

```

Now what if we wanted to have these shapes randomly move up and down, is there a place we could introduce variables in these rectangles to have them bounce up and down while still remaining locked on the their X axis? 

```
let a = 200
let b = 200
let c = 200
let d = 200

function setup(){
    createCanvas(400, 400)
}

function draw(){
   background(255)
   rect(100, a, 100, 100)
   rect(200, b, 100, 100)
   rect(300, c, 100, 100)
   rect(400, d, 100, 100)

}

```
Great! Yea we could use variables in the place of the yPos pararmeter for the rectangle. Now, how could we represent these 4 rectangles in such a way that would take up less of our time, is there a way we could automate that replication of these rectangeles?

```
let a = 200
let b = 200
let c = 200
let d = 200

function setup(){
    createCanvas(400, 400)
}

function draw(){
     
     let i = 1
     while(i <= 4){
     rect(100 * i, a, 100, 100)
     i ++
     }
}

```
OK this is great, but can anyone isolate a problem with this approach? Now all of our variables have the same value, but they could very easily have extremely different values. How could we refer to each and every one of these variables while still using the convenience of a while loop? This is where the magic of arrays come in. First lets go ahead and create an array so that we can hold all of these values in a list. Declaring our array is just like declaring any variable, depending on where we declare it it has a different **scope**. Just like we have global variables and local variables we can have arrays which are accesses locally or globally. We declare them much in the same way we'd declar a variable.

```

let arr = []

```

This is what you would call an empty array. By making *arr* equal to these two empty brackets I've told the computer that arr is in fact an array, but that right now it is empty. Anything that we put in between these brackets, as seperated by commas are whats inside our array. We can add things inside of the arrray immediately or we can add things to the array after the fact.

```
let arr = [200]
```

```
let arr = []
arr.push(200)
```

```
let arr = []
arr[0] = 200
```

All of the examples above are the same, and you'll want to use different ways of adding to arrays in different circumstances. That last one might be a bit tricky and brings up something we haven't talked about before, how a computer counts! The first entry in our array is at index 0, the second number in our array is at index 1, and on and on. The way that we refer to a specific value is by referencing its array. Go ahead and console.log(arr[0]). 
So we have lots of ways to add our four variables to this array, for the sake of simplicity lets go ahead and add them like this:

```
let arr = [200, 200, 200, 200]
```

But now that we have this array which is filled with different variables is there a way that we can access it inside of our while loop? Take a look and see if you can think of a way.

- hmmmmmmm
- hmmmmmmmmmmm
- hmmmmmmmmmmmmmm
- hmmmmmmmmmmmmmmmm
- hmmmmmmmmmmmmmmmmmm
- hmmmmmmmmmmmmmmmmmmmm

```
let arr = [200, 200, 200, 200];

function setup() {
  createCanvas(400, 400);
}

function draw() {
  let i = 0;
  while (i <= 4) {
    rect(50 + i * 50, arr[i], 50, 50);
    i++;
  }
}
```
Is there anything we can do to get each of the squares to move? See if you can add to the arr[i] variable in such a way that is reminiscent of us adding onto posX. If you've figured this out, can you figure out a way to have each of the 4 squares have an their own independent speed using another array, and without using i as the speed your increasing. The answer is below.

```
let arr = [200, 200, 200, 200];
let speeds = [1, 2, 3, 4]

function setup() {
  createCanvas(400, 400);
}

function draw() {
  let i = 0;
  while (i <= 4) {
    arr[i] += speeds[i]
    rect(50 + i * 50, arr[i], 50, 50);
    i++;
  }
}
```
Can you find a way for these shapes to return to the top once they have scrolled past height? (its easier than you think).
```
let arr = [200, 200, 200, 200];
let speeds = [1, 2, 3, 4]

function setup() {
  createCanvas(400, 400);
}

function draw() {
  let i = 0;
  while (i <= 4) {
    arr[i] += speeds[i]
    
    rect(50 + i * 50, arr[i], 50, 50);
    if(arr[i] > height){
    arr[i] = 0
    }
    i++;
  }
}
```
Can you make 8 of the squares on the page with a range of speeds and conditional statements which will keep them scrolling forever. Here's an example of how someone might implement that. 

### [Many Moving Objects](https://editor.p5js.org/dunkFig/sketches/BtqrIXgPM)
Play around with this a little bit, the truth is that learning how to use arrays easily is going to make your life a TON easier. With that said, lets move on to **CREATING OUR OWN FUNCTIONS**


## Our Own Functions
So lets talk about some of the functions that we often use in p5:
- draw
- setup
- keyPressed
- mousePressed

How are these functions usually setup, lets take a look at the setup function below and identify a few parts:

```
function setup(){

}
```
So first off we've written out function, which tells javascript that the next thing that we're going to create is a function. Next we have the name of that function, in this case it's setup, but if we were making our own function it could be *anything we want it to be*. Next we have two sets of parenthases which we'll talk about last, and then we have the curly brackets which contain everything inside of the function. 
I could also make a function that looks like this:

```
function tree(){
  fill(50, 200, 50)
  triangle(200, 100, 100, 300, 300, 300)
  rect(190, 300, 20, 40)
}
```
Now once I *call* this function it will do everything inside of the function. the way that I call the function is just by writing its name, followed by the two parenthases afterwards. Once we've written a function we don't have to write function at the beginning of it anymore, just like we don't have to say let in front of a variable every time after we've declared it. I've gone ahead and called this inside of the draw loop. Tak a look below and make your own function that creates a more complex shape.

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  tree()
}

function tree(){
  fill(50, 200, 50)
  triangle(200, 100, 100, 300, 300, 300)
  rect(190, 300, 20, 40)
}

```
Now one of the really exciting things is that we can actually pass values into a function so that we can use the same information of the function over again and again, with a slightly different input. Lets use this tree example as a starting point. first lets start off by calling the tree function everytime we click the mouse on the canvas, as opposed to in the draw loop.

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}

function tree(){
  fill(50, 200, 50)
  triangle(200, 100, 100, 300, 300, 300)
  rect(190, 300, 20, 40)
}

function mousePressed(){
tree()
}

```
Lets also get rid of the background in the draw loop so we can actually see whats going on:


```
function setup() {
  createCanvas(400, 400);
}

function draw() {
}

function tree() {
  fill(50, 200, 50);
  triangle(200, 100, 100, 300, 300, 300);
  rect(190, 300, 20, 40);
}

function mousePressed() {
  tree();
}
```
Great! But this is kind of boring right? Lets push some parameters into this function so that we can dynamically change where we want this tree to be!

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
}

function tree(x, y) {
  fill(50, 200, 50);
  rect(x - 10, y + 100 , 20, 40);
  triangle(x, y, x - 50, y + 100, x+ 50, y + 100);
  
}

function mousePressed() {
  tree(mouseX, mouseY);
}
```
You can Also view this example [here](https://editor.p5js.org/dunkFig/sketches/KsuhL4u6C)
Why don't you take some time to create another function, and make a way to toglle back and forth between them every time the mouse is pressed. If your stumped you can go ahead and look at the answer below, is there a way that you can update an array with all of the X positions and Y positions of the objects you have on the canvas?:

### [Castles & Bulls (Our Own Functions)](https://editor.p5js.org/dunkFig/sketches/uDjnazT6B)

This is not easy, so great work on working through some of these problems today! The last thing that I want us to do is to look at this example right here Theres a few things that are new in this program, but I think for the most part you should be able to understand this. I want everyone to:

- Open this sketch
- Duplicate it so its saved in your p5 editor
- Slowly work through the entire sketch and comment in what makes sense to you

### [Moving Spheres](https://editor.p5js.org/dunkFig/sketches/i_yHJv26m)

