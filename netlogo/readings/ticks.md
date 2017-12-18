# Ticks
NetLogo can keep track of time using a unit called a tick.

## Commands
[`ticks`](#ticks) <br/>
[`tick`](#tick) <br/>
[`reset-ticks`](#reset-ticks)

### ticks
`ticks` is a keyword that reports the current value of the tick counter.

### tick
Running the `tick` command increases the value of the tick counter by 1.

### reset-ticks
In order to initialize or start the tick counter, you must run the `reset-ticks` command.

### Sample Code
The code below is all you need to get the tick counter increasing by 1 every second.
```
to setup
  reset-ticks
end

to go
  every 1 [
    tick
  ]
end
```

### Exercises
1. Get the background of the NetLogo interface to repeatedly change from green to yellow to red. DO NOT use the `wait` command. It should spend 7 seconds being green, 3 seconds yellow, and 5 seconds red.
2. Create a squirrel-shaped turtle. The squirrel moves forward .1 every .1 seconds. Every time you click on the NetLogo interface, an acorn is created at the location of the mouse click. The squirrel will then face the acorn, move towards it and eat the acorn. Integrate a time delay for how often you can place an acorn. You have to wait at least 5 seconds before you're able to place another acorn.
