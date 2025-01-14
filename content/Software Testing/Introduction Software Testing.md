### objectives
- find bugs
- address bug and how to categorize it
- levels of testing

### software testing?
testing all aspects of software and all usage cases from the user
- test for requirements are met
- find defects
- prevent defects --> find bugs as early as possible
- maintain quality of software
- help meet standards
- provide information for decision making
create test cases and apply it to software

### why testing is necesary?

1992 software error 42 billions dollars

win by number under bottle

company by mistake printed the winning number on all the bottles and paid billions in settlements

**errors cost alot**


### myths
- second class career -- no it is very respected
- he has to test programs only -- test requirements and documentation
- manual testing -- automation testing, etc.
- boring -- innovation

### objectives again
- find all bugs and document them
- bug error failure
- why is it called bug
- sources
- excercise
- terms
- myths again

### problems
bug -> deviation from result
-  error: mistake from person so bug/fault appears, might cause failure in software
we need to test multiple test cases to make sure there is no bugs

we need software specification
- objective of client
- requirements of client
- document includes all description of any type
### specification bug
when the programmer does what is required but what is required didn't cover entirely what the programmer should have done

without specification we have:
- standards in industry
- communication with peers
- statistics
- life experience 

> We test using valid and invalid input

> [!info] Myth
> ### Testers must make sure that 100% of the software is error free
> No, if they test for every case in existence they will take decades to test
 
> [!info] Myth
> ### Testers are judged by how many bugs they find
> No, they're only judged by working software

---
### table of contents
- what is test case
- differ between test case and suite
- main attributes of test case
- maintenance of test case
- two tips for writing test cases

### what is bug addressing?
- register bug in a bug tracking tool
	- which module this bug belongs to
	- assigned to whom
	- we can easily revise if the bug is solved or not
- bug addressing process
	- bug reporting
	- bug fixing
	- recheck if bug fix made new bugs

Bug tools could be as simple as excel sheet

Test case is written by tester to test the software and tries to find if **expected result** is the same as real result

test suite is collection of test cases related to each other

### test case spreadsheet
- unique ID
- priority
- description
- additional info
- ER
- procedure
- revision history

### maintainability of test case
- create repeated actions in sperate documents
- don't build test case on information that might be changed

---
### table of contents
- [[#unit/component/module testing]]
- [[#integration testing]]
- system testing
- acceptance testing
### unit/component/module testing
function/port/sql
unit does as specified

after coding the developer himself does unit coding 

it's for faster debugging because we're testing small bits of code

### integration testing
when combining modules with each other.
if not all units of code not fninished then integration tester does dummy code
we also sometimes use commercial units of code that werent tested

#### big bang testing
combing all unit modules and testing them together
#### bottom up testing
combining into layers and testing them
#### top down testing
opposite to prior method

### drivers and stubs / scaffolding
drivers are used in [[#bottom up testing]] 

#### drivers
they are top level dummy code that is made to test bottom layer code

#### stubs
when low level functions aren't finished and we need to test upper level functions

### system testing
afer software is done

input and outputs
functional and non funtional requirements
test cases are done from the specification manual
- non functional testiong
	- stress testing (users eg.)
	- volume testing
	- configuration testing
	- compatibility test
	- timing testing
	- security testing
	- environmental testing
### acceptance testing
end user gets to test the system
- alpha test (client tests the software where developer is present)
- beta test (without developer present)
---
test design techniques

### introduction
- design suitable test case for each software
- right number of test cases to cover code possibilities
- effective number of effective test cases 

### table of contents
- black box testing
	- equivilence partitioning
	- boundry value analysis
	- decision table
	- state transition
	- use case
- white box testing
	- statement testing
	- decision testing

### test to pass
software does the minimum requiremets assumes that the user uses the program as intended
### test to fail
uses strategy that extracts weaknesses in software and intend to get failures out of software
### black box testing
without seeing the internal structure of the system
relies on seeing if output is correct relating to the input
assumes user has no technical knowledge

#### equivilence partitioning 
range of data test
if 1 to 100 numbers to test the program
valid partition and invalid partition
create two test cases from both of the above

#### boundery value analysis
first number in the range and last number in the range
numbers and dates

#### decision table
busines rules in a table with conditions

#### states 
using state diagram and state table

#### use case
preconditions of actor before getting on software
post condition state of system after actor used it and acquired his goals
broad main functionality technique 
### white box testing / structure based testing
can see the system internal and has source code
sees if all avenues of the program the compiler passes through it or not
useful got unit testing and integration testing

#### statement testing
all statements are tested or executed 
#### decision testing
write test cases with all possibilities of code branching