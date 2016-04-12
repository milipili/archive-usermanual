Shebang
=======

> A shebang (also called a sha-bang, hashbang, pound-bang, or hash-pling), is the
> character sequence consisting of the characters number sign and exclamation mark
> (that is, "#!") at the beginning of a script.

_source:_ [Wikipedia](https://en.wikipedia.org/wiki/Shebang_%28Unix%29)


Scripting with Nany on UNIX platforms
-------------------------------------

Shebang are allowed (and ignored) in any Nany source file[^1]. So, on UNIX,
it is possible to transform a Nany script file as executable.

Here is an example Nany file:
```bash
bash$ cat ./my-script
#!nanyc -x

public func main: i32
{
    console << "Message from a Nany script !\n";
    return 0;
}
```

Setting file permissions using `chmod`:
```
bash$ chmod +x ./my-script
```

Running out script, like any executable:
```
bash$ ./my-script
Message from a Nany script !
```



[^1]: Shebang must be placed at the very bottom of the script