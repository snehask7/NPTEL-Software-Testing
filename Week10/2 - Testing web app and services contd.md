# Week 10 
-------------------------------------------------------------------
# Testing of web applications and web services contd (client side)
https://onlinecourses.nptel.ac.in/noc20_cs77/unit?unit=70&lesson=72
-------------------------------------------------------------------

**Testing dynamic web apps**
* web server is where all software resides, and web page is dynamically generated based on client interaction
* testing can be done on client or server side

**Client side testing (black box)**
* Tester has no access to data on the server
* Client and server are completely seperate

* Client provides inputs (html form elements)
* Inputs can be chosen or generated
* Generated from previous user sessions (very effective)
* Supplied by tester
* Generated randomly (not very effective)
* Bypass testing: values that violate constraints on inputs
* Problem is not all screens are accessible

**Test value selection**
* Values within domain are needed. Not efficient to generate all possible inputs
* Generating random values is not effective
* Very hard to automatically generate values
* User data might be innefective from testing point of view
* Tester supplied inputs might be expensive
* Study the application and construct a set of values

**Bypass testing**
* Webapps impose constraints on inputs through HTML forms
  * Client side validation using script (check input data before sending to server)
  * Use explicit attributes with html form tags
* Bypass testing creates inputs that violate validation rules and are directly sent to server thereby bypassing client side validation
* let tester save and modify the HTML
* Remove any client side validation scripts or attributes added to tags to restrict inputs
* Can see how the server reacts to these invalid inputs
* Bypass testing can also be done at the server side
* safer to do it at the client side since server data might get corrupted

**Validation rules examples**
* violate size restriction
* Use values not present in the dropdown
* violate hard coded values
* use values that cause javascript errors
* Change get to post or vice versa
* Change destination URL

**server side constraints**
* data type conversion
* data format validation
* inter field validation

**Security violation**
* empty string
* commas
* tag symbols
* dir paths



    




