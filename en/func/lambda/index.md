Lamda
=====

Function in **Nany** can be rewritten in anonymous form and assigned to a variable.

```
public func main
{
    var msg = "message: ";
    var f = func (x) -> msg + s;
    console << f("hello world");
}

```

And it guarantees the life time of variable as long as it is still used:
```
// --- func generator --

func generator(coeff)
    -> func (x) -> x * coeff;

public func main
{
    var f1 = generator(2);
    console << f1(4);  // 8

    var f2 = generator(8.42);
    console << f2(2);  // 16.84
}

```