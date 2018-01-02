## Exam03

### Questions
1. Assume you have three global variables: hours, minutes, and seconds that are a reflection of ticks. However in your new NetLogo world, one second is really 0.001 seconds. Write a button named `bigbang` that clears the tick counter. Write a `go` forever button that progresses time accordingly. Include in your go button the logic to update the value of hours, minutes, and seconds. For example, after 18.607 seconds have passed after clicking the `go` button, the hours should have a value of 5, minutes 10, and seconds 7.
2. Randomly generate 10 blue color patches. Create 8 turtles and randomly distribute them. Ask each turtle to move to the closest blue colored patch.  
3. Musical Chairs
4. Click Time = Patch color  





Tic Tac Toe
|X|O|X|
|O|X|O|
|O|O|X|
Assume that you have a 3x3 world already set up that consists of only 9 patches. Assume you have turtle shapes `X` and `O` to use. Write a `go` forever button that will handle the logic of a tic-tac-toe game. When you click on a patch, a piece(turtle) will be placed on that patch. The turtle will be shaped as an `X` or `O` depending on whose turn it is. You can only click on a patch where a piece has not been placed.

Musical Patches
Assume you have 5 brown colored patches randomly placed in the world and 6 randomly placed turtles. Create a forever `go` button that commands each turtle to move towards the closest unoccupied patch. Once a turtle has reached a brown colored patch, no other turtles can occupy that patch. The one turtle that doesn't make it to a brown patch dies. Use the following conditions for turtle movement:
- have the `go` procedure run every .01 seconds
- have turtles move forward .1 with each `go`

Card Matching
Assume that you have a 4x4 world that consists of 16 patches. Create a `setup` procedure that assigns two random patches the same color. Once a patch has been assigned a color, it cannot be assigned another color. Write a `go` forever button that handles the game logic. When you click on a patch, it'll reveal its assigned color. When you click on two patches with the same assigned color, both will stay revealed. Otherwise, the two patches that you clicked on will return to being black. 

Tocks
Create your own timing system in NetLogo. Create the following:
* `reset-tocks` - should behave like `reset-ticks`
* `tocks` - should behave like `tocks`
* `tock` - should behave like `tock`

Randomly Placed Squares
Assume that you have a resized world that has the bounds of -25 25 -25 25. Write a `draw` procedure that randomly places four 5x5 blue colored squares in each quadrant of the world. The squares should all be contained within the world. They should not be cut off by the edge of the world. If you use modular design, it will save you time.
