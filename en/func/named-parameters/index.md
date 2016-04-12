Named parameters
================

You can use named parameters, so by calling the function 
it's not necessary to respect the order of parameters:

```
func power(base, exponent): any
{
    var res = base;
    
    for (each i in [: 2..exponent :])
        res *= res;
        
    return res;
}

public func main
{
    console << power(5, 2);                  // display 25
    console << power(exponent:2, base:5);    // display 25
}

```

This feature helps resolving the function call, you can consider it's part of function signature:

```
func load(memory)
{
    console << “loading content from memory content: \(memory) \n”;
}

func load(fileurl)
{
    console << “loading content from url: \(url) \n”;
}



public func main
{
    load(memory: “hello world”);
    load(file: :url{http://nany.io/index.html});
    
    load(“123password”); // compile error!
}

```


Note: you should avoid to mix index parameter system with named parameter system.
If you have to, remember that while you don't use the named parameter system, 
compiler uses the index parameters system, but once you name the parameters, 
you name all the rest parameters til the end.

```
func aFunc(a, b, c, d, e, f):any -> a + b + c + d + e;

public func main
{
    console << aFunc(1, 2, 3, 4, 5);           // OK
    console << aFunc(e:5, a:1, d:4, b:2, c:3); // OK
    console << aFunc(1, 2, d:4, e:5, c:3);     // OK: a = 1, b = 2. c, d and e are present
    console << aFunc(1, b:2, 4, e:5, c:3);     // KO: a = 1, b = 2. from the 3rd parameter compiler cannot solve 
    console << aFunc(1, 2, a:4, e:5, b:3);     // KO: a and b are used in both index and named parameter systems. c and d are absent
}

```