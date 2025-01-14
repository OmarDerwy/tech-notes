
# 1	intro

![[Pasted image 20241110034522.png]]
![[20190313_CH01_L01_SW testing life cycle P1.mkv]]

## 1.1	STLC 
![[Pasted image 20241110034629.png]]
![[Pasted image 20241110072717.png]]
After that we decide on testing types like functional and non-functional
requirements could be in the form of software document, use cases, uml diagrams

after than test planning
![[Pasted image 20241110073004.png]]

test plan document is produced after this step

what is in scope/ out of scope? what the portion of project / modules we need to focus on

in test case development the tester begins writing the test cases
![[Pasted image 20241110073601.png]]
for each test case the tester writes test data

we also have the requirement traceability matrix. an excel sheet which connect test conditions with the test case, and code. through this we create the impact analysis

tester created the test cases before the developer finishes the code

---
![[20190205_CH01_L02_SW testing life cycle P2.mkv]]

environment setup. we set up the hardware / software that we need for testing

build setup / configuration manager
test cases imported
test execution
then does smoke testing: opens website and randomly navigate to see if it's working or not
test cases are then worked on in each module
estimate time
pass or fail
report bug in bug tracking tool

then we create status report
![[Pasted image 20241110074537.png]]
developer pushes new build with fixed bugs / new features
check if bugs were solved
test new modules
regression testing
test cycle closure > acceptance testing > deliver UAT docuement (user acceptance testing)

>[!note]
> in some cases we use agile methodology so client is present in each iteration of the project
> after each iteration we create project status report and let the client know the known issues

---
![[20190205_CH02_L01_What is test cases and it's format？.mkv]]
test case writing: writing bad test cases will create bad test results which will produce bad code.

how to write effective test cases
for example: sign in form
resuse test cases in all sign in forms in the future

test case: docuumentation to specified inputs and predicted results. group of execution conditions, ar / er // group of activities with ar / er while defining execution
![[Pasted image 20241110075513.png]]
SRS document or user story, etc.
![[Pasted image 20241110075541.png]]
SRS function and non-functional specified by client and should be reviewed before starting work.

test case attributes:
- unique id
- test case title
- summary
- precondition
- test steps
- test data
- expected result
- actual result
- status fail or no
- comments

---
![[20190205_CH02_L02_TC： ID (Naming Convention).mkv]]test case ID
TC_001 > problem
better use naming convention
TC_projectname_module_###

---
![[20190205_CH02_L03_TC Description.mkv]]test case description

describe simply what the test case does
![[Pasted image 20241110080119.png]]

---
![[20190205_CH02_L04_TC pre-condition.mkv]]

precondition / assumption

user data applied like account logged in
dependencies in a certain environment

if we test buying a production then precondition that it exists in the shopping cart
![[Pasted image 20241110080327.png]]
![[Pasted image 20241110080426.png]]

we must execute precondition before execute test case

---
![[20190205_CH02_L05_Test Data Types.mkv]]test data inputs
makes your life easy as tester
prepared before developer finishes code
can be used more than once during execution
without test data you might not be able to execute test case

negative data
trying invalid email that is incorrect

if we have a big range we create specific values that makes me cover it.

if client specified data and prepare data before test case

---
![[20190205_CH02_L06_TC Steps.mkv]]steps

points of verification during execution 
![[Pasted image 20241110080949.png]]

the steps to execute test case without ambiguity

every verification points has to have an expected result

![[Pasted image 20241110081222.png]]
![[Pasted image 20241110081233.png]]

---
![[20190205_CH02_L07_TC Expected Result.mkv]]
expected result

very important

could be an attachment or screenshot

---

![[20190205_CH02_L08_TC statues , priority , actual result.mkv]]
status: pass fail not applicable

test case priority: critical, high, medium low > SRS

actual result

---
![[20190205_CH03_L01_bug report attributes.mkv]]bug report

![[Pasted image 20241110081625.png]]
bug ID: unique problem, module, environment

steps
expected result
actual results
severity > SRS
priority
attachment > screenshot or video

---
![[20190205_CH03_L02_Bug life cycle.mkv]]bug life cycle

![[Pasted image 20241110081951.png]]
other status is
- defered > cannot solve in this build
- duplicate
- known issue
---
![[20190829_Ch04 _L01_Practical example on test case writing.mkv]]
practical example

test case writing

login page in facebook

expected result shouls be extrapolated from SRS document

---
![[20190829_Ch04_l02_ Practical example on bug reporting.mkv]]

practical example on bug report


---


![[20190829_Ch04_l03_suggestions for more practice.mkv]]

Guru99 > live project