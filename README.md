# colourramp
R code to create colour ramps with some colour-blindness support

make a colour ramp:

```R
ramp <- colour_ramp(list("black", "red", "light blue"))
```

and get 6 colours out of it:

```R
ramp(6)
```

You can make a colour ramp which works better for colourblind
individuals using the `collapse_red_green` or `collapse_blue_yellow`
flags:

```R
ramp <- colour_ramp(list("black", "red", "light blue"), collapse_red_green = TRUE)
```

This will give a ramp which puts more colours along blue-yellow parts
of the ramp than red-green. If you have a `red` node next to a `green` node,
this will likely still give a ramp that is not too friendly to red-green
colourblind individuals, though, so use with care.
