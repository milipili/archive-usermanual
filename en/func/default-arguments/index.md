Default arguments
=================

You can define the default values for function arguments, 
so if there's no value passed in the function, the default value will be used.

```
func display(msg = "this is a default message")
{
    console << "Display message: " << msg;
}

func main()
{
    display("Hello Nany"); // "Display message: Hello Nany"
    display();             // "Display message: this is a default message"
}

```

