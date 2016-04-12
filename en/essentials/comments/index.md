Comments
========

Comments are statements that will not be compiled. They are annotations for
other programmers or small descriptions of what your code does,



Declaration
-----------

In Nany, comments can be written in 2 different ways:

 * Line starting with `//`:
```
// This is a comment, it will be ignored by the compiler
var x = "this is a variable defined in a statement";
```

 * Section of code starting with `/*` and ending with `*/`.
   this method is used for multi-line comments:
```
/*
This is a multi-line comment,
it will be ignored by the interpreter
*/
var x = "this is a variable defined in a statement";
```


Documentation
-------------

Comments, in combination with some special tags, can be used for
self-documenting code:

```cpp
/*!
** \brief Compute the sum of two values
**
** \param a Any value that supports the operation '+'
** \param b Any value that supports the operation '+'
** \return The sum of \p a and \p b
*/
func sum(a) -> a + b;
```