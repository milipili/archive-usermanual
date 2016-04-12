Constructor and Destructor
==========================
Constructor is a method which performs initialization of every object. Destructor is a method which is automatically invoked when the object is destroyed.

Constructor
-----------

**new** keyword is used to call class constructor. 
The same keyword is used to define the constructor.



The following codes are valid since compiler makes a default constructor for you:

```
class Vehicle 
{
    var wheels = 4;
    var headlamps = 2;
    var horn = true;
}

public func main
{
    var vehicule = new Vehicule;
}
```

User can add an user-defined constructors (with the arguments), in this case it becomes the default constructor:

```
class Vehicle 
{
    //! Constructor with arguments
    operator new(wheels, headlamps)
    {
        self.wheels = wheels;
        self.headlamps = headlamps;
        // self.horn remains true.
    }
    
    var wheels = 4;
    var headlamps = 2;
    var horn = true;
}

public func main
{
    var vehicule = new Vehicule(wheels: 2, headlamps: 1);
    var vehicule2 = new Vehicule; // compile error!
}
```
There is a more elegant way to replace the following code:
```
    operator new(wheels, headlamps)
    {
        self.wheels = wheels;
        self.headlamps = headlamps;
    }
```
by using **self** and the same variable member names in the parameters zone for the automatic assignations:

```
class Vehicle 
{
    operator new(self wheels, self headlamps) {}
    
    var wheels = 4;
    var headlamps = 2;
    var horn = true;
}

```

Once an user-defined constructor with arguments is defined, it becomes the default constructor. If you want to use the constructor without argument, you have to define it:

```
class Vehicle 
{
    //! Constructor by default
    operator new {}
    
    //! Constructor with arguments
    operator new(self wheels, self headlamps) {}

    var wheels = 4;
    var headlamps = 2;
    var horn = true;
}

public func main
{
    var vehicule = new Vehicule; // No more compile error
}
```




Destructor
----------

Normally you don't need to define destructor explicitly (compiler makes it for you). In some case you have to define it explicitly by using **release** keyword.

```
class Mutex
{
    //! Constructor by default
    operator new
    {
        pmtx = std.native.pthread.mutex_create();
    }

    operator release
    {
        std.native.pthread.mutex_destroy(pmtx);
    }
    
    ...

private:
    var pmtx = null;
}

```

