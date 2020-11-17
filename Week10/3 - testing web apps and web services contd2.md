# Week 10 
-------------------------------------------------------------------
# Testing of web applications and web services contd (server side)
-------------------------------------------------------------------

**Server responses**
* Errors at server could cause permanent database damage if not recognized (**Exposure**)
* Valid responses
  * Ignores invalid input
  * Provides error message which is generic or specific
* **Faults and failures**: invalid input cause abnormal server error

**Server side testing (white box)**
* use normal graph models if server code is available
* control flow graph only used with static models
* Presentation layer of web app is used for testing
* 2 graph models for software in **presentation layer**
  * Component interaction model
  * application transition graph 
 
**Atomic sections***
* We look at server side code present in the presentation layer
* sections are dynamically generated and sent from server to the client
* Atomic section has the property that if one part of the section is sent to the client, the entire section is.
* Atomic section can include javascriot 
* atomic section can be empty
* **Content variable is when data is generated dynamically**

**Graph models**
* Component interaction model (CIM)
  * models individual components
  * combines atomic sections
  * intra-component: interactions within a component
  * nodes are atomic sections
  * transitions tell how to move from one section to another
* Application transition graph(ATG)
  * Each node is a CIM
  * edges are transitions among CIM
  * inter component
  
**Component expressions**
* Atomic sections are combined to model dynamically generated web pages
* 4 ways to combine and gegerate component expressions:
  * Sequence P1.P2 (P1 then P2)
  * Selection P1|P2 (p1 or p2)
  * Iteration P1* (P1 0 or more times)
  * aggregation P1 {P2} (p2 is included in p1)
* algos can automatically generate these expressions

**Transitions in Component interaction model**
* Simple link transition (HTML Link)
* Form link (Form submission)
* Component expression transition (Execution of a component causes a component expression to be sent to client)
* Operational Transition (sudden unplanned input; ex: back, forward, refresh, user edits url, broswer reloads from cache)
* Redirect transition (server side transition not visible to user)

**Video for CIM example and ATG example 22 minutes**

  
  
