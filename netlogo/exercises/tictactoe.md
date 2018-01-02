```
globals [turn]

to setup
  ca
  resize-world -1 1 -1 1
  set-patch-size 100
end

to go
  every .1 [
    if mouse-down? [
      ask patch mouse-xcor mouse-ycor [
        if count turtles-here = 0 [
          sprout 1 [
            ifelse turn mod 2 = 0 [
              set color white
              set shape "x"
            ][
              set color white
              set shape "circle 2"
            ]
            set turn turn + 1
          ]
        ]
      ]
    ]
  ]
end
```
