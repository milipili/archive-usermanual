Array
=====

Array is a common random access data type of collection of elements.

If you already know all the elements in the array, you can declare your array statically.

```
var list = ["Array", "in", "Nany"];
```

Otherwise, you can use operator **new** to initialize your empty array
and then append the elements dynamically afterward.

```
var list = new string[];
list.append("Array");
list.append("in");
list.append("Nany");
```

You can also declare your array statically and append the elements dynamically at any time.

```
var arr = [2, 5, 8];
arr.append(3);
arr.append(6);
arr.append(9);

```

