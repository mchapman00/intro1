# Lists
NetLogo can keep track of time using a unit called a tick.

## Commands
[`list`](#list) <br/>
[`fput/lput`](#fput/lput) <br/>
[`item`](#item) <br/>
[`length`](#length) <br/>
[`but-first/but-last`](#but-first/but-last)

### list
- creates a list out of 2 elements
- making a list of any size other than 2 requires parentheses <br/>
How to make a list of size 2
```
list random 10 random 20
```
How to make a list of size 1
```
(list random 10)
```
How to make a list of size greater than 2
```
(list random 10 random 20 random 30)
```

### fput/lput
- lists cannot be changed so in order to add elements to a list, you need to make a copy
- `fput/lput` creates a copy a list with a new element added to either the front or back of the list
```
let stuff [1 2 3 4]
set stuff2 lput stuff 5
set stuff3 fput stuff 5
show stuff               
show stuff2       
show stuff3        
```
What will `stuff`, `stuff2`, and `stuff3` print respectively?

### item
- gives you the element at the index or position specified
```
let primes [2 3 5 7 11]
show item 3 primes  
```

### length
- gives you the number of elements found in a list
```
let primes [2 3 5 7 11]
show length primes
```

### but-first/but-last
- produces a copy of a list with either the first or last element removed
```
let stuff [1 2 3 4]
let front but-first stuff
let back but-last stuff
```

### Mini-Lab - Move & Undo
* turtles-own [ move-list ]
* setup button
    - creates one turtle, make move-list an empty list
    - set the shape to person    
    - change the patch color of the origin to white

* up/down/left/right buttons:
    - when pressed, they cause the turtle to move in a direction
    - add the word "up" "down" "left" or "right" to your list (based on which button was pressed)
    - change the patch color of the new position to white.
* undo button
    - should 'undo' the last move, and remove it from the list. You need the but-first or but-last command.
    - this resets the patch color AND the position of the turtle.
    - should do nothing when there are no more moves left.

#### How it should work
1. You click setup, up, up, right, up.
You now have 5 white patches, and the Turtle has move-list of: ["up","up","right","up"]
The world looks like:
```
 W <-turtle is here
WW
W
W <- origin here
```
2. You press undo for the first time:
You now have 4 white patches, and the Turtle has move-list of: ["up","up","right"]
The world looks like:
```
WW <-turtle is on the right W
W
W <- origin here
```
3. You press undo a second time:
You now have 3 white patches, and the Turtle has move-list of: ["up","up"]
The world looks like:
```
W <-turtle is here
W
W <- origin here
```
