Properties
==========
Properties are the values associated with an object or a build-in type in Nany. You use value (a special variable within properties for only setter), get and set to define how to get and set the property values.

Properties in a class:

```
class Window
{
public:
    var width -> mWidth; // getter/setter automatic
    var height -> mHeight;
    var surface -> {get: width * height}; // getter only, read-only property
    var borderSize -> {get: mBorderSize};

private:
   func setBorderSize(value)
   {
       if (value < 1)
           raise "border size must be strictly greater than 0";
       mBorderSize = value;
   }

private:
    var mWidth = 50;
    var mHeight = 25;
    var mborderSize = 1;
}

func main()
{
    var w = new Window;
    console << "w width: " << w.width; // "w width: 50"
    console << "w height: " << w.height; // "w height: 25"
    console << "w surface: " << w.surface; // "w surface: 1250"
    w.width = 5;
    console << "w surface: " << w.surface; // "w surface: 125"
    
    w.borderSize = 5; // compiling error
}
    
```

[Properties with build-in types](../../var/properties/index.md)