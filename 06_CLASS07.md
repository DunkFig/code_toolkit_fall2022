
# CLASS 07 (Lists and our own functions)
### Lets start off with some current events:
-[Imageine Science Film Festival]()
-[Mezzanine Play Through at the New Museum]()
-[My Deep Fake Dad]()

### HOMEWORK
[HomeWork Roster]()

### MIDTERM IDEAS


### Review of Last week 
- Millis()
- State

### Refering to many things!
Today we're going to finally be getting in to storing information which we can later refer to in our sketches. There are many ways and systems that we can use to store information, the array being the simplest way. First lets take a look at a few examples thhat use lists to refer to tons of variable and shapes at the same time. 
[Flocking 2D]()
[Flocking 3D (Gene Kogan)]()

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
