# Cannon
Build a cannon that shoots projectiles a distance proportional to the amount of time clicking on the cannon.

## Instructions
1. Make a cannon breed and a projectile breed. The cannon and projectiles should have a heading of 315.
2. When you click and hold onto a cannon, you should be able to drag it around and move it. You should be able to drag the cannon with a mouse within a radius of 3.
3. When you click and hold onto the cannon for 3 or more seconds and then release, the projectile it shoots should be able to travel across the entire length of the world no matter where it is. (hint: think of the longest distance you can travel within a square or rectangle)
4. Holding onto the cannon for any time less than 3 seconds should shoot a projectile a distance proportional to the time. For example, if you were to hold the cannon for 2 seconds, the projectile it shoots will be able to travel 2/3 the max distance. (hint: pythagorean theorem)
5. If a projectile reaches the edge of the world, it should disappear.

### Mini-Steps
See if you can create two global variables that keep track of when you start clicking the mouse and how long you've been clicking on the mouse.

### Extra
Create three robot cannons that move around randomly and shoot at you.

### Scaffold
```
breed [cannons cannon]
breed [bullets bullet]
;wasMouseDown? keeps track of the previous state of the mouse for comparison
globals [wasMouseDown?]
;you need to calculate how far a bullet
;is supposed to travel when you create one
;and store it in a variable

to setup
  ;insert your setup stuff
  reset-ticks
  set wasMouseDown? false
end

;HEY LOOK HERE - there's only one every!!! Everything is inside of that one every!
to go
  every .1 [
    tick
    cannonBehavior
    bulletBehavior
  ]
end

;
to bulletBehavior
  ask bullets [
    fd .1
    let futurex [pxcor] of patch-ahead 1
    let futurey [pycor] of patch-ahead 1
    if futurex = max-pxcor or futurex = min-pxcor or
       futurey = max-pycor or futurey = min-pycor [
      die
    ]
    ;you need a way to tell a bullet to stop
  ]
end

;reports the diagonal length of the world
to-report diagonal
  let a (abs min-pxcor) + max-pxcor
  let b (abs min-pycor) + max-pycor
  report sqrt ((a * a) + (b * b))
end

to cannonBehavior
  ifelse mouse-down? [
    ;what if the mouse is down now and wasn't down before?
    ask patch mouse-xcor mouse-ycor [
      if any? cannons in-radius 3 [
        ;what should wasMouseDown? be set to here
        ask cannons [setxy mouse-xcor mouse-ycor]
      ]
    ]

  ]
  [if wasMouseDown? [
       ;what do you do if the mouse was down before, but isn't down now?

    ]
    ;what should wasMouseDown? be set to here?
  ]
end  
```
