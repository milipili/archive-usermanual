while loop
==========
```
while <expr> do <stmt>

```

```
var n = 3;
while n < 0 do
{
    console << "it's final countdown: " << n;
    n -= 1;
}

```
In case you need to execute at least once some instructions, you can use do while loop:
```
do <stmt> while <expr>

```

```
var n = 0;
do
{
    console << "it's executed at least one time whatever n value is.";
    n -= 1;
}
while n < 0

```

