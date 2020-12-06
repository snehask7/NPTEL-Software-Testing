#Week 10 
-----------------------------------------------------------------
#Testing of OO Applications
https://onlinecourses.nptel.ac.in/noc20_cs77/unit?unit=70&lesson=74
-----------------------------------------------------------------

**Abstraction**
* Classes used to represent abstraction
* inheritance, polymorphism, dynamic binding also support abstraction
* new types created by abstraction are descendants of existing types  
  2 new types  
  * extension: class extends parent if new method name and doesn't override any method in ancestor
  * class refines parent if new behavior provided which is not in overriden method, and doesnt call overriden method

**inheritance**
* sub type inheritance (aka substitution principle): If class B uses sub-type inheritance from class A, it is possible to freely substitute any instance of 
B for A and still satisfy a client of A. B has a is-a relationship with A
* sub-class inheritance: Descendant can reuse methods and variables from ancestor without having to ensure descendant instances meet ancestor specifications

**polyphormic methods**
* If class B inherits from class A, and A and B defne a method m, m is polymorphic
* if an object x is declared to be of type A, then during execution x can be of type A or B and the version executed depends on the current actual type of the object
* Collection of methods that can be executed are called polymorphic call set: ex: {A:m(),B:m()}

**4 levels of class testing**
* intra-method: testing a particular method
* inter-method: interaction between methods are tested
* intra-class: testing within a class
* inter-class: interaction between classes is tested

**Visualizing OO interactions**
* Assume a class encapsulates all state info required as a collection of state variables

**CONTINUE FROM 18 minutes**





