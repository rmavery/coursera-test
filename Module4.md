# JavaScript



## Defining Variables, Functions, Scope
### Variables are dynamically typed


### Variable Scope
* Everything is executed in an *Execution Context* 
* Function invocation creates a new *Execution Context* 
* Each *Execution Context* has: 
  * Its own Variable Environment
  * Special 'this' object 
  * Reference to its *Outer Environment* 
* Global scope does not have an *Outer Environment* as it's the most outer there is

```
Referenced (not defined) variable will be searched for 
in its current scope first.  If not found, the Outer Reference
will be searched.   If not found, the Outer Reference's Outer Reference 
will be searched, etc.  This will keep going until the Global Scope. 
If not found in the Global scope, the variable is undefined. 
```

In the following scenario, it will print 'x = 2' because even though A() calls B(), B()'s outer reference is Global, not function A().
What matters as far as variable scope, is where that function is defined.  
```
var x = 2;

A(){
  var x = 5;
  B();
} 

B(){
  console.log(x); 
}
```

