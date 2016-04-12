Declaration
===========

Function declaration is in the following form: 
**func** - the keyword for function, followed function name, parameter list, 
return value type (optional) and its definition.



```
func power2(n): any
{
   return n * n;
}

```

Note that brackets are used for delimiting the definition. If there is only one line 
in the function definition, you can compact your function by writing it without 
bracket ( "->" means "return") :

```
func power2(n) -> n * n;
    
```

Of course, you can use a defined function in another function definition:

```
func power4(n) -> power2(n) * power2(n);

```

The type of return value can be ignored if there's no returned value (**void**).

```
func runAway()
{
    console << "Q: What happened to the function that ran away?"
    console << "A: It never returned.";
}

```
