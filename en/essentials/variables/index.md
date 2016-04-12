Variables
=========

Users soon notice that the usage of variables in **Nany** is intuitive and that
no effort is required to type them, because the compiler types variables for you. 
It releases programmers from the frustrating syntax so they can focus on semantics 
of their program. It doesn't mean that you are free to do the dirty and incoherent 
code - the first assignment of your variable decides the type of this variable, 
then compiler ensures it remains the same type during its lifetime. 

The following code will not be compiled and the compiler will stop on the last line:
```
var myVar = "Answer to the Ultimate Question of Life, the Universe, and Everything";
// some code
myVar = 42; // <- compiling error! Not because 42 is a big nonsense (actually, it is) 
            // but because of the wrong type of variable "myVar"
```


You can, of course, declare the type of your variable:
```
var languageName: string = "nany.io";
var version: f64 = 1.0;
var introduced: i32 = 2015;
var isAwesome: bool = true;
```

