return
======

When **Nany** reaches a return statement, the function will stop executing.

If the function was invoked from a statement, **Nany** will "return" to execute the code after the invoking statement.

A return value to be passed back to the code that called the function, if a return value type has been specified in definition of function.

```
func sum(x, y) : i32
{
    return x + y;
}

```

You can, however, use a compact way to express return:

```
func sum(x, y) : i32
    -> x + y;

```