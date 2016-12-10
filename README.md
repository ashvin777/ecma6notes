# ecma6notes

**ECMA Script 6** 

**Arrow Expression and Lexical This**

 -  Arrow functions doesn't have its own `this` or `arguments` implicit object. They share it from the parent environments functions only.  Even if it can't access the object property with `this` directly. To access it should be inside a function of the object. 

**Class** 

 - Supports inheritance, super calls, instance, static methods(Prototype) and constructors
 - Supports extends and ?implements?
 - If `class B extends A` then in constructor of class B have to call the class A constructor first to access the same `this` using `super(params);` syntax.
 
**Enhanced Object Literals**
 
 - Function key name is not required. Function can be directly defined.
 - Can have computer dynamic property names. Like `[ "prop_" + (() => 42)() ]: 42`

