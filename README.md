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

    // list matching
    var [a, ,b] = [1,2,3];
    a === 1;
    b === 3;
    
    // object matching
    var { op: a, lhs: { op: b }, rhs: c }
           = getASTNode()
    
    // object matching shorthand
    // binds `op`, `lhs` and `rhs` in scope
    var {op, lhs, rhs} = getASTNode()
    
    // Can be used in parameter position
    function g({name: x}) {
      console.log(x);
    }
    g({name: 5})
    
    // Fail-soft destructuring
    var [a] = [];
    a === undefined;
    
    // Fail-soft destructuring with defaults
    var [a = 1] = [];
    a === 1;
    
    // Destructuring + defaults arguments
    function r({x, y, w = 10, h = 10}) {
      return x + y + w + h;
    }
    r({x:1, y:2}) === 23

 - List item

