# Week 10 
-----------------------------------------------------------------
# Testing of OO Applications
https://onlinecourses.nptel.ac.in/noc20_cs77/unit?unit=70&lesson=74
-----------------------------------------------------------------

**Abstraction**
* Classes used to represent abstraction
* inheritance, polymorphism, dynamic binding also support abstraction
* new types created by abstraction are descendants of existing types  
  2 new types  
  * extension: class extends parent if new method name introduced and doesn't override any method in ancestor
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
* Class is static entity  
* Interactions between clsases and methods are difficult to visualize  
* If a class V extends W and there is a method m which is overriden in V, and if a new object o is created and o=new V() and o=new W() are executed conditionally based on the value of another variable b, whether m in V or m in W is executed deponds on the value of b so we cannot visualize which method is executed  
* Data flow anomoly: a variable needed by one method might not be available because it may have been defined in the parent class method which was not executed and instead an overriden child class method was only executed  
  
**Yo-Yo Graph**  
* Understanding which version of a method will be executed is difficult adn executions can bounce up and down between inheritance levels  
* Yo-Yo graph has a root and descendants. Nodes are methods, edges are method calls  
* Methods include new, inherited and overrden methods  
* directed edge is from caller to callee  
* Each class in graph is given a level in the graph and it shows the actual calls made if an object has the actual type of that level. these are in bold arrows  
* Dashed arrows are calls that cannot be made due to overriding  
* example in ppt  
  
**Faults in OO programs**  
* Less static determinism as when one method calls another, overriden can happen so it is not static and is dynamic  
* Inheritance and polymorphism yield vertical and dynamic integration  
* Assume that Instances of descendant can be substituted for instances of tha ancestor  
* 9 kinds of faults/anomolies  
  * ITU: inconsistent type use - descendent class does not override any inherited method. if class C extends T and C adds new methods, object can be used as both T and C and methods in T might make object go to state that is inconsistent for C  
  * SDA: State definition anomaly - state interactions of descendant not consistent with ancestor. Class X extends W and X overrides methods in W, but variables that are defined by a overriden method may never be defined because the overriding method is executed instead and other functions may use the variable that must have been defined by the overriden method  
  * SDIH: State definition inconsistency - Local variable introduced in class definition and name is same as another inherited variable. Local variable is only referred to unless super.v used (hidden variable). Anomoly if method defines local variable and sends to another method in a different class which is expecting inherited variable from ancestor  
  * SDI: State defined incorrectly - overriding method defines same variable that overriden method defines.  
  * SVA: State visibility anomaly: X extends W and Y extends X. W may have a private variable which is not visible by descendant but needs to be used by descendant overriding method  
  * IISD: indirect inconsistent state definition - descendent adds extension method that defines inherited state variable  
  * ACB1: Anomalous construction behavior 1  
  * ACB2: Anomalous construction behavior 2  
  * IC: Incomplete construction


