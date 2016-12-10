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

**Template Strings**

 - Can use multi line strings.
 - Can use object names directly inside the template string with syntax `${this.name}`
 
**Destructuring**

 - Can assign object into object or Array into Array. 
 - Can set default values
 - Can use it in functions
 - Difference in the use of : and = in the left hand assignment side. = take assign the values to keys but : assign the values to property value(object name on right side)

    var {x, y, w = 10, h = 10} = { x : 10, y : 20, w: 44};
    console.log(x, y, w , h);
    var {name: x} = { name : 10 };
    console.log(name, x);

**Default + Rest + Spread**

 - Default - like in function param assign the param with a value to make that defaul value if not passed or undefined in function call.
 - Rest - in function rest can be access via ... sign. Like `function(x, ...y)`. So everything apart from the first param will go inside ...y object in an array. And can be access inside function with y object name itself.
 - Vice versa while passing param to function call the same notation can be used. We can pass param in Array via `functionCall(..[1,2,3])`

**Let + Const**

 - Let is block level scope variables
 - Const can't be changed later and will throw if changed.
  
**Iterators + For..Of**

**Generators**
 
 - Use `function*` and `yield` combinations. yield return or throws Generator class reference to the callee. Generator has all those iterations methods defined inside it prototype.  It is used for iteration only. Along with `Symbol.iteration`

**Unicode**

 - Support Unicode characters into the JavaScript code. 
  
**Modules**
 - List item
