# Ticks Solutions

## Exercise 1
Get the background of the NetLogo interface to repeatedly change from green to yellow to red. DO NOT use the `wait` command. It should spend 7 seconds being green, 3 seconds yellow, and 5 seconds red. <br/>

Using `mod`
```
to shiftColor [newColor]
  ask patches [set pcolor newColor]
end

to setup
  shiftColor green
  reset-ticks
end

to go
  every 1 [
    let time (ticks mod 15)
    if time = 6 [shiftColor yellow]
    if time = 9 [shiftColor red]
    if time = 14 [shiftColor green]
    tick
  ]
end
```

Using `reset-ticks`
```
to shiftColor [newColor]
  ask patches [set pcolor newColor]
end

to setup
  shiftColor green
  reset-ticks
end

to go
  every 1 [
    if ticks = 7 [shiftColor yellow]
    if ticks = 10 [shiftColor red]
    if ticks = 15 [
      shiftColor green
      reset-ticks
    ]
    tick
  ]
end
```
