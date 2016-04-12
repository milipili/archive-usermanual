for loop
========

```
for <var> in <set> do <stmt> [else <stmt>]
```
Flow controller **else** is optional. You can use it to prevent from that the flow doesn't enter at all into for loop.
```
// without else
for i in [0, 1, 2, 3] do
    console << i;
    
// with else 
var list = new int[];
for value in list do
    console << value << "\n";
else
    console << "the list is empty\n";

```


Loops and ranges
----------------

```
for i in [:0..10:[ do
    console << i; // 0 to 9
```