Switch
======
Syntax
------
```
switch <var|expr> do
{
    case <const>:   <stmt>
    case <const>:   <stmt>
    ...
    [default:       <stmt>]
}


// use the comma between the case if you want to use the same procedure on the different cases.
switch <var|expr> do
{
    case <const1>,
    case <const2>:    <stmt> // process for const1 & const2 
    case <const3>:    <stmt> // process for const3
    ...
    [default:       <stmt>]
}

```
Note that there's no need to use break for switch instruction - all the execution will stop before next case (or default). If you want to use the same procedure on the different cases, put the comma between/among your cases.

Example
-------

```
var lang = getSystemLang();

switch lang do
{
    case "mc", // Monaco
    case "fr": // France
        console << "Bienvenu";

    case "hk", // Hongkong
    case "sb", // Singapore
    case "tw": // Taiwan
        console << "歡迎";

    default:
        console << "Welcome";
}
```