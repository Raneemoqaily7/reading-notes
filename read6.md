# How to use the Random Module in Python
 The random module provides access to functions that support many operations

 ### Random Functions
 * randint 
 Used to generate integers between Twoo parameters,  first value should be less than the second one
 example:
 import random
 print random.randint(10, 20)

 * Random
 example:
 import random
random.random() * 50 //// To get  larger number, just multiply it.

* choice 
Generate a random value from the sequence
example:
random.choice( ['one', 'two', 'three'] ) // you will get random choice either one , two or three

* Shuffle
shuffles the elements in list in place, so they are in a random order (reorder)
example :
list =["one","two","three"]

From random import shuffle
shuffle(list)
output==> ["three","one","two"]  // each time result will vary

* Randrange

import random
for i in range(6):
    print random.randrange(1, 59, 4)

start = 1  
stop 59 
step =5

# What is Risk Analysis in Software Testing and how to perform it?

* It helps to highlights the potential problem areas After knowing about the risk areas, it helps the developers and managers to mitigate the risks. 
possible risks that you could encounter:

Use of new hardware
Use of new technology
Use of new automation tool
The sequence of code
Availability of test resources for the application

* Risk Identification


Business Risks:  It is the risk that may come from your company or your customer, not from your project.

Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

Software Risks: You should be well versed with the risks associated with the software development process.

* Risk Assessment
 This step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically.


* The perspective of Risk Assessment


Effect

Cause

Likelihood

* How to perform Risk Analysis?


Searching the risk

Analyzing the impact of each individual risk

Measures for the risk identified

# Test Coverage
You can always move slow tests to a later stage in your deployment pipeline, or even pull them out of the pipeline and run them periodically. Doing these things will slow down the feedback from those tests, but that's part of the trade-off of build times versus test confidence.
[Back Main](./README.md)


