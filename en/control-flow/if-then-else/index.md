Conditional Evaluation: If-then-else
====================================


The `if` statement
------------------

Definition:
```
if <expr> then <stmt> [else <stmt>]
```
If the condition expression `<expr>` is true, then the corresponding
`<then>` block is evaluated, otherwise it will be the `<else>` block.


Inline `if`
-----------

`if` is by definition a statement, but it can be used within any expression
as well (like the c++ ternary operator), like for example conditional assignment:

```
var x = if a < b then a else b;
```

Or conditional function calling:

```
(if a < b then a else b).draw();
```





Optional binding
----------------

```
if var <id> = <expr> then <stmt> [else <stmt>]
if (var <id> = <expr>) <op> <expr> then <stmt> [else <stmt>]
```

```
if (var x = a + b) > c then
    console << "x is greater than c: " << x;
else
    console << "x is less or equal than c: " << x;
```