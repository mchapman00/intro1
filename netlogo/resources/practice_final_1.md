# Practice Final 1

1. [3pts] What value will be printed by the following commands? (choose the best answer)
```
let a [12  5  3  45]
let i 0
let answer item 0 a
repeat length a [
	if (item i a) < answer [set answer item i a]
	set i i + 1
]
show answer
```
A) 0		B) 12		C) 5		    D) 3			E) 45


2. [3pts] If the following commands are executed:
```
ask patches [
   	ifelse abs pxcor = abs pycor
 	    [  set pcolor white]
 	    [  set pcolor black]
]
```
Which of the following shapes will you see: (choose the best answer)
A) one diagonal back line		B) one diagonal white line
C) a single white patch			D) a white “+”			E) a white “X”

3. [3pts] If turtle F and turtle G use different turn methods as follows:
```
to TurnF
     rt random 3
     lt random 3
end

to TurnG
    rt (random 5) - 2
end
```
Which of the following is true?   (choose the best answer)
a) Turtle F has a higher chance to remain at the same heading, compared to G.
b) Turtle G has a higher chance to turn right, compared to F
c) Turtles F and G will have the same possible outcomes, and probabilities.
d) Turtle F has more possible resulting directions compared to Turtle G.

4. [6pts] Write code to create 100 turtles, placing those turtles on random locations such that no two turtles are on the same patch, and no turtle is on a red patch. (assume at least 100 patches are non-red, and there are no existing turtles).

5. [6pts] Write code (you needn’t make it into a procedure) to ask the two turtles: turtle 4 and turtle 19, to swap their colors.

6. [4pts] Create the My-Median reporter that will be given a list of numbers which are already in increasing order, and that the list has an odd number of elements (like 3 numbers or 157 numbers in it).  The reporter should calculate and give back the median of the list.  Yes, Netlogo has a median function.  No, you may not use it.
```
to-report my-median [my-list]
  ; your excellent code
end
```

7. [6pts] Create a procedure called Border that will create a red border around the Netlogo world, a single patch wide.  Do not assume that the world has 33 x 33 patches, but you may assume that the patch in the center of the world has coordinates (0,0).

8. [5pts] The named colors, (like red, green, blue, sky, magenta, etc.) in the Netlogo color palette have the values: 5, 15, 25, 35, 45, 55, 65, 75, 85, 95, 105, 115, 125, 135.  Create a reporter called RandomColor that will report a random one of these colors with equal probability.  You may not use either of the commands, one-of or n-of.

9. [8pts] Assume that we have two breeds: Zombies and Humans. The zombies and humans have a somewhat difficult time coexisting (except on Mr. K’s t-shirts).  Write the procedure called FantasyOfK that compares the number of zombies and humans on each patch, and decides what to do based on these actions:  
-More zombies than humans on the patch makes the humans on the patch die.  
-More humans than zombies on the patch makes the zombies on the patch die.  
-The same number of zombies and humans on the patch:
80% chance: All the zombies AND humans on the patch die
20% chance: that they all survive.

10. [6pts] Create a Go (forever) procedure that does the following: if the mouse cursor is in the Netlogo world and the mouse button is down, it should be dragging turtle 0 around wherever it goes, except when the mouse is pointing at a red patch. Turtle 0 cannot be dragged onto a red patch.

11. [4 points Extra credit] Create a procedure called PatchBorder that will draw a border around every patch in the world (do not assume that it’s necessarily a 33 x 33 world).  The desired color of the border will be given as a parameter:
```
to patchBorder [border-color]
		; your superb code
end
```
