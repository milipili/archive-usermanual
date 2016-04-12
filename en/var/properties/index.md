Properties
==========
Properties are the values associated with an object or a build-in type in **Nany**. You use **value** (a special variable within properties for only setter),
**get** and **set** to define how to get and set the property values.

Properties with build-in types:
```
var radius = 4.0;
var diameter -> {get: radius * 2, set: radius = value / 2}; 
var circumference 
    -> {get: std.math.pi * diameter, set: diameter = value / std.math.pi};

console << radius; // display 4
console << diameter; // display 8

circumference = 15; // will automatically update the radius 15/3.1415926

console << radius; // display (15/pi)/2

```

[Properties in a class](../../class/properties/index.md)

