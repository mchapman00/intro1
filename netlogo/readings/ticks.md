# Ticks
NetLogo keeps track of time using

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

### Exercises
1. Get the background of the NetLogo interface to repeatedly change from green to yellow to red. DO NOT use the `wait` command. It should spend 7 seconds green, 3 seconds yellow, and 5 seconds red.
<br/>
2. Create a turtle shaped as a squirrel. It moves forward 1 every .1 seconds. Every time you click on the NetLogo interface, create an acorn. The squirrel will then face the acorn and move towards it. Integrate a time delay for how often you can place an acorn. You have to wait at least 5 seconds before you're able to place another acorn.
