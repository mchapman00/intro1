# Lab 05 - Zombies

### New Commands
`face` <br/>
`min-one-of` <br/>
`distance` <br/>

### Helpful Commands
`set-default-shape <BREEDS> "SHAPENAME"` <br/>
`create-<BREEDS>`


### Examples
Making new breeds of turtles
```
breed [players player]
breed [monsters monster]
```

Creating new breeds
```
to setup
  ca
  set-default-shape monsters "turtle"
  create-monsters 8 [
    set color 10 * random 13 + 5
    setxy random-xcor random-ycor
  ]
  create-players 1 [ set shape "person" set color green]
  ask turtles [ set size 3]
end
```

Standard go button
```
to go
  every 1 / 30 [
    ask turtles[
      fd .1
      rt random 5
      lt random 5
    ]
  ]
end
```

Printing out all the distances between two agents
```
to showdistances
  ;the player has to ask the monsters, so the monsters can use
  ;myself to refer to the player
  ask players[
   ask monsters[ show distance myself]
  ]
end
```

Targeting the agent within an agentset with the smallest value of a specific property
```
to makeOneBig
  ask min-one-of monsters [color] [set size 5]
end
```

Asking turtles to face another turtle
```
to facePrevious
  ask turtles[
    if who > 0 [
      face turtle (who - 1)
    ]
  ]
end
```

Asking turtles to face a patch
```
to facePatch
  ;if???
  ask turtles[
    face one-of patches with [pcolor = white]
  ]
end
```

## Instructions
1. Make two breeds: zombies and humans

2. Make two buttons
* Setup:
    - Make 2 zombies and 5 humans.
    - They should all be person shaped.
    - Place them around the world randomly.
    - Zombies should be green.
    - Humans should be blue.

* Go:
    - Zombies perform the zombieBehavior function.
    - Humans perform humanBehavior function.

3. Human Behavior: wiggle randomly (for now)

4. Zombie behavior: Identify and follow the closest person. Use the commands `face` and `min-one-of`. The speed should be the same as the wiggle speed.

5. Modify the zombie behavior: ONLY FOLLOW the closest person if they are in a 10 unit radius. When there are no people nearby, they should just wiggle.

6. Change their detection ability from a radius of 10, into a cone of 10 units / 90 degrees in front of the zombie.

7. Modify the humans to run away from the closest zombie.

8. Modify the humans to run away from the closest zombie within a 12 unit radius.
