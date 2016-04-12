Member access control
=====================
Any member in a class has an accessibility level, which defines how the member can be accessed from outside of your class. You can use the following access key words to specify the accessibility of a type or member when you declare it. If no accessibility level is defined, **public** is the default accessibility level.

public
------
The type or member can be accessed by any other code inside and outside of class.


protected
---------
The type or member can be accessed only by code in the same class, or in a class that is derived from that class.


internal
--------
The type or member can be accessed by any code in the same library/module, but not from another library/module.


private
-------
The type or member can be accessed only by code in the same class.