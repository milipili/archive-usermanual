Each loop
=========

```
each <var> in <set>
```

The `each` expr behaves as if a for loop was placed before the current statement:
```
console << (each i in [0, 1, 2, 3]);
```
is strictly equivalent to:
```
for i in in [0, 1, 2, 3] do
    console << i;
```


Loops and ranges
----------------

Like with `for` loops, ranges can be very handy:
```
var sum += each i in [:0..10:[;
```