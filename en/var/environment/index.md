Environment variables
=====================

Environment variables are a set of dynamic named values that can have
various effects on a program's behavior.



Quick access
------------

Environment variables can be directly manipulated (read and writing)
using the `$` character as standard string variables like in any shell script:

```
// copy the value of the env variable 'HOME'
var home = $HOME;

// set or reset the env variable 'EDITOR'
$EDITOR = "vim";
```


Manipulating the values of environment variables
------------------------------------------------

Determine whether an environment variable is set or not:
```
if std.env.contains($EDITOR) then
    console << "EDITOR = " << $EDITOR;
```

Set/Unset an environment variable using mere strings:
```
std.env.unset("EDITOR");
std.env.set("HTTP_PROXY", "http://proxy:80");
```


Complex variable names
---------------------

Sometimes, the name of an environment variable is not known in advance.
It can be constructed using standard string manipulations:
```
var s = "SSH_AUTH";
console << $[s + "_SOCK"];
```




Iterating through environment variables
---------------------------------------

The variable `std.env.variables` behaves like a container:
```
console << (each v in std.env.variables).name << " = " << v.value;
```




Scope
-----

Any modification of an environment variable is only visible to the
current process. It can affect the child process too if the environment
variables are preserved.