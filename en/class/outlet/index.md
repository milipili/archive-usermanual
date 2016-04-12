Outlet
======
Outlet is a very convenient feature in Nany. 
It allows users to override a method of a class from outside of class 
without following the classic procedure of inheritance.

```
class Logger
{
    operator << (x): ref
    {
        append(x);
        return self;
    }

    [[outlet]] func append(v)
    {
        assert(false, "type not handled");
    }
}

[[plug]] func Logger.append(v: string)
{
    console << v;
}

[[plug]] func Logger.append(v: boolean)
{
    console << (if v then "true" else "false");
}

public func main
{
    var logger = new Logger;
    logger << "hello" << " world: " << true;
}


```