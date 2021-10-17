# NPTEL-Software-Testing
## Week 1   
* Introduction to software testing  
* Popular examples of faults due to lack of testing  
* Types of software  
* Maturity levels in testing  
* Testing terminologies 
* Types of testing  
* RIPR  
* Model based testing  
* Test requirement and criterias  
* Generator and recognizer  
* jUnit  
* prefix and postfix values  
* Assertions  
* jUnit used for system testing  

  
## Week 2  
* Basics of graphs, reachability, test path,touring  
* Types of coverage criteris  
  * Structural coverage criteria  
  * Data flow coverage criteria  
* Structural coverage criteria  
  * Node coverage  
  * Edge coverage  
  * Edge pair coverage  
  * Path coverage  
    * Complete path coverage/specified path coverage    
    * Prime path coverage  
    * Complete round trip coverage/specified path coverage  
    * Simple round trip coverage  
  * Tour with side trips and detours  
  * Structural coverage criteria subsumtion  
* BFS  
* DFS (paranthesis theorem), types of edges  
* Strongly connected components  
* Algorithm for finding prime paths   
    
```diff  
- round trip coverage and why it does not subsume node coverage  
```  
## Week 3  
* defs and uses  
* def clear path  
* data flow coverage criteria  
  * All defs coverage  
  * All uses coverage  
  * All du paths coverage  
* CFG for code  
* Code coverage  
* Cyclomatic complexity  
* Basis path testing: testing each linearly independent path  
* DD Path and 5 conditions  
```diff  
- 3rd lecture last example why extra path in test path for prime path coverage  
```  
## Week 4  
* Data flow coverage example for a test code  
* Test paths from DU pairs  
* What is integration testing  
* Types of interfaces  
* Types of interface errors  
* Scaffolding  
* 5 Approaches to integration testing  
  * incremental  
  * top down  
  * bottom up  
  * sandwich  
  * big bang  
* Structural Coverage criteria with integration testing  
  * Node coverage covers all modules  
  * Edge coverage covers all calls between modules  
  * Path coverage for sequence of calls  
* OO call coverage and OO Object call coverage  
* Data flow coverage criteria with integration testing  
  * Caller, callee, call site, actual and former parameter  
  * Coupling variable  
  * Types of coupling  
    * Parameter  
    * Shared data  
    * External device  
  * Last def, first use  
  * Coverage criteria  
    * All coupling def  
    * All coupling use  
    * All coupling du path  
  * Transitive du pair  
* Specification testing and graph coverage  
  * Design specification describes what behavior software must exhibit  
  * Sequencing constraints impose constraints on the order in which methods may be called  
  * Consider CFG and find paths violating constraints  
  * Sometimes memory needed so FSM used for state behavior  
* Coverage Criteria for FSM  
  * Node,edge,edge pair  
  * data flow coverage gets complex  
* precondition  
* triggers  
* Testers need to generate fsm on their own  
* In summary, Graphs have both structural coverage criterias and data flow coverage. Source code can be modelled using CFG and CGF with defs and uses. Design modelled using call graphs and coupling du pairs. Specifications are modelled using sequencing constraints and FSM  
  
## Week 5  

```diff  
-Week 6 2021 assignment last 3 questions?  
```  
  
  

