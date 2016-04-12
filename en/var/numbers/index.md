Integers and Floating-Point numbers
===================================


Integer
-------
Any number that can be written without a fractional component. It could be signed or unsigned.

```
var i = 10;
var j = 0u; // unsigned 0

func answerToUltimateQuestion(): u32 -> 42;

func makeArray(arrSize: u64): array
{
    return new array(arrSize);
}

```


Floating-Point number
---------------------
Any number can contain a fractional part.  It could be signed or unsigned.

```
func pi(): f32 -> 3.1415926;

func squarRoot(nbrToSqrt: f64): f64 -> std.math.sqrt(nbrToSqrt);

```