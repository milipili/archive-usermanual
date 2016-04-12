continue
========
Forces transfer of control to the controlling expression of the smallest enclosing

```
foreach v in [0..9]
{
    if v != 5 then
        continue;

    console << v;       // display 5. This statement is skipped each time v!=5 
}
```
