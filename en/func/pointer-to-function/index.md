Pointer to function
===================

A pointer to function is a variable that stores the address of a function 
that can later be called through that function pointer.

```
func foo -> 69;

func poo
{
   var f = foo;
   return f(); // return 69
}

```