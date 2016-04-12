Operators
=========


Assignment
----------
The operator used for assignment.
```
// =

var isNanyAwesome = true;

var myFaroritePosition = 69;

```

Comparison
----------
Comparison operators allow you to compare two values, and return a boolean value.

```
// <
if val < 10 then
    console << "val is inferior to 10";

// <=
if val <= 10 then
    console << "val is inferior or equal to 10";

// >
if val > 10 then
    console << "val is superior to 10";

// >=
if val >= 10 then
    console << "val is superior or equal to 10";

// ==
if val == 10 then
    console << "val is equal to 10";
    

```

Arithmetic
----------
Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value.

```
// +   : Addition 
var i = i + 3;

// -   : Subtraction
var j -= 5;

// *   : Multiplication
func 2power2() -> 2 * 2;

// /   : division
console << "49 / 5 = " << 49 / 5;

// mod : modulo
var weekDay = (randomNumber() mod 7) + 1;

```

Logic
-----
Logical operators are typically used with Boolean (logical) values. 

```
// or
while expr1 or expr2
    doAction();
    
// and
if expr1 and expr2
    doAction;

// not
if not expr
    doAction;

```

Constrained
-----------
Constrained operator gives a constrained condition for whichever type.

```
// | : such as
func fibonacci(n)
    -> fibonacci(n - 1) + fibonacci(n - 2)
func fibonacci(n: any | n < 2) // parameter n could be any value, but conform with the condition n < 2 - on the other words n should be 1 or 0
    -> n
    
func append(v: f64 | v >= 0.0)
{
    console << "v must be a positive float point number";
}


```


Stream
------
```
// >>
// <<

console << "Thanks to stream operator used by console object, I can display this message.";

```
