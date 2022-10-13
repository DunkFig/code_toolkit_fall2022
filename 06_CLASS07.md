
# CLASS 07 (Lists and our own functions)
### Lets start off with some current events:
- [Imageine Science Film Festival]()
- [Mezzanine Play Through at the New Museum]()
- [My Deep Fake Dad]()

### HOMEWORK
[HomeWork Roster]()

### MIDTERM IDEAS


### Review of Last week 
- Millis()
- State

### Refering to many things!
Today we're going to finally be getting in to storing information which we can later refer to in our sketches. There are many ways and systems that we can use to store information, the array being the simplest way. First lets take a look at a few examples thhat use lists to refer to tons of variable and shapes at the same time. 
- [Flocking 2D]()
- [Flocking 3D (Gene Kogan)]()

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
