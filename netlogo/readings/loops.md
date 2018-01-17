# Loops
Loops are a fundamental concept in computer science.

### `while`  
In the code below, the command block is repeatedly run so long as the boolean expression is true. If the boolean expression is never set to false, the command block will run forever resulting in what's called an infinite loop.
```
while [boolean-expression] [
  command block
]
```

### How to Make a Loop
There are three main parts to making a loop
* counter
* boolean expression
* increment / decrement
In the code below, the variable `x` serves as the counter. The inequality `x > 0` is the boolean expression and the increment/decrement, `set x x - 1` is within the command block.
```
to countdown [n]
  let x n
  while [x > 0] [
    show x
    set x x - 1
  ]
end
```
To print out all the elements in a list
```
to listPrint [ L ]
  let i 0
  while [ i < length L ] [
     show item i L
     set i i + 1
  ]
end
```
