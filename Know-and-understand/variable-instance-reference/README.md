



# #Differences among C# Variable, Instance (Object) and Reference
***1. Variables in C#***
 --   A variable represents a storage location in memory. It has a name by which you can refer to it at compile time, and at execution time it has a value, which will always be compatible with its compile-time type. (For example, if you've got a  `Button`  variable, the value will always be a reference to an object of type  `Button`  or some subclass - or the  `null`  reference.)

***1. Instance (Object) in C#***
   An object is a sort of separate entity. Importantly, the value of a variable or any expression is  _never_  an object, only a reference. An object effectively consists of:
		    -   Fields (the state)
		    -   A type reference (can never change through the lifetime of the object)
		    -   A monitor (for synchronization)

***1. reference in C#***
  A reference is a value used to access an object - e.g. to call methods on it, access fields etc. You typically navigate the reference with the  `.`  operator. For example, if  `foo`  is a  `Person`  variable,  `foo.getAddress().getLength()`  would take the value of  `foo`  (a reference) and call  `getAddress()`  on the object that that reference refers to. The result might be a  `String`  reference... we then call  `getLength()`  on the object that  _that_  reference refers to.
