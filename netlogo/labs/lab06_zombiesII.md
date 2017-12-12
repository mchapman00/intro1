### Helpful Commands
`in-radius` <br/>
`any?` <br/>
`min-one-of` <br/>   
`max-one-of` <br/>
`face` <br/>

###Examples
To see if there are any things in a 5 unit radius
```
if any? things in-radius 5[
   do stuff
]
```

To face a specific thing
```
face thing
```

To face away, turn around after facing it. To find the closest thing and turn it red
```
if any? things [  
  ask min-one-of things [distance myself] [ set color red ]
]
```

## Instructions
DO NOT move on to the next part until ALL previous numbers are complete.

For PART2: For each of the numbered objectives:
    Write the number.
    Since this section has more complex objectives, you can break it down into several chunks. (Write all the chunks at once)
    Check off each chunk as you complete it.
Modifications to lab:

9. Change the following settings:
* World size: 51 by 51 (set max-xcor to 25)
* Turtle sizes: 3
* Wiggle speed: 0.1
* Zombies range in value from green to (green + 2) in decimals.
* Humans range in value from orange to (orange + 2) in decimals.

10. Miscellaneous (Use the sliders in your code, to replace your original default numbers!!!!)
* Make Sliders for
    - starting_zombies (1-20)
    - starting_humans (1-100)
    - maximum_stamina (20-100)
    - zombie_vision_radius (1-10)
    - zombie_vision_angle (10-360)
    - human_vision_radius (1-10)
* Humans have a stamina variable and start with maximum_stamina upon setup.

* Make Monitors for:
    - the number of zombies
    - the number of humans

* Your project should run at an appropriate speed.

11. Zombie Behavior:
* When there is a human in a cone of zombie-vision-radius (make a slider), zombie-vision-angle (make a slider) the Zombies chase after the closest human at a speed of 0.3 Otherwise they shamble. Shamble is a slow wiggle (move forward at 0.07, and modify the angle randomly +/- 20 degrees).
* When a zombie catches a person (the person is on the same patch as the zombie):
    - the person dies
    - a new zombie is created.
    - This new zombie turn 90 degrees from the heading of the original zombie so they separate quickly

12. Human Behavior when they don't see a zombie:
  * Humans normally wiggle at a speed of 0.2, angle at +/- 20 randomly.
  * When a person wiggles, they also they gain 0.2 stamina (but no more than maximum_stamina )
13.  Human Behavior when they see a zombie:
    * When one or more zombies are closer than human_vision_radius units away, they try to run from the zombies.
    * When a person is running they check their stamina:
        When there is 1 or more stamina, the person moves away from the nearest zombie at speed 0.8, they lose 1 stamina.
        When there is less than 1 stamina, the person moves away from the nearest zombie at speed 0.1 (do not recover stamina here)

####OPTIONAL
[DO NOT USE THE SHAPES EDITOR IN CLASS!!!! (unless you are 100% done) ]
a) Make different custom shapes (“zombie” , "uglyZombie" etc) in the shapes editor (don't spend too much time on this) Make sure you duplicate the “person” shape instead of just editing it, or you will lose the person shape.
b) Use the multiple zombie shapes to make an animation if you want to practice animations using turtle shapes. They can cycle between 2-3 shapes when moving.
