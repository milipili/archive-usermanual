Reference
=========
Reference allows user use a variable to refer to another variable (use keyword **ref**) , 
instead of copying only the value (by using **var**).

Consider the following code:
```
var a = 666;

var x = a;
console << x; // 666

ref y = a;
console << y; // 666

x = x + 1;
console << x; // 667
console << a; // 666

y = y - 1;
console << x; // 667
console << a; // 664
console << y; // 664

```
You can see "a" and "y" are the different names of the same variable.