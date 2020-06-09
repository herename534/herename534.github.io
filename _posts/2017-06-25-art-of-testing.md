---
   layout: post
   title:  "The art of software testing by Glenford Myers -- a summary"
   date: 2017-08-20 8:16:01 +0200
   categories: books
   tags: philosophy, books, summary
   published: true
   language: English
---

I really liked the book because from what it seems to me, it gives a good
overview of testing in general, and, especially, the psychology of testing.

Below I'd like to point out the key moments from there. 

<!--excerpt-->

#### Basic definition of testing, psychology of testing, the mindset for testing

* Testing is a process of executing a program with an intent of finding bugs

* It should be done to improve the quality of the program

* A psychological aspect of testing is very important -- you should assume
the program has errors, or otherwise you wouldn't be able to detect as many.
Also it should be done by other person that the one who wrote it

* Any program, even a simple one could contain many errors, little bugs or
unpredicted situations, it's not possible to detect all bugs in a program

* Most of the times, it's not possible and it's not smart to exhaustively test
all the possible paths in a program, so the purpose of testing should be to
maximize the number of errors found with finite test cases

* A good and successful test case is the one that finds errors


#### Types of testing

| *criteria*                                          | *types* |
| :---:                                               | :---:   |
| who tests the program                               |   manual testing and automated testing    |
| whether the internal structure of a program matters | black box testing and white box testing    |
| what is tested                                      |  unit tests, integration tests, system testing, acceptance testing, functional testing, installation testing  |


* There're two types of testing regarding if the tester knows or cares
about internal structure of a program. It could be treated as a **black box**,
where only input and output matters. Or there's also a **white box testing**
when the tester cares about internal structure of a program and tests it out
as well

* Also there're methods of testing performed manually by humans and automated
testing

##### **Subtypes of human testing**:

* _Group code inspections_,

* _Group walkthroughs_, 

* _Peer evaluations_

##### **Subtypes of unit testing**:

* _Incremental_, where each module is tested
with the ones that passed tests and 

* _Non incremental_ where each module is tested
separately

* _Top-down_ unit testing, where the testing starts from root module and
goes down to the others and 

* There's _bottom-up_ unit testing which starts with the bottom module and moves up

##### **Functional testing**:

* _Functional testing_ is a type of testing aiming to find errors and bugs in how the
program behaves compared to the enternal specification, from the end user's point of
view

##### **System testing**:

* System testing targets mismatches in a program compared to the program's objectives.
If there's some feature specified that isn't properly implemented

* _Facility testing_ (to find out the missing features) 

* _Volume testing_ (when the program is fed with large amounts of data)

* _Stress testing_ is a type of system testing when the program has to deal with large
amounts of data over a short period of time

* _Usability testing_ is another type of system testing

##### **Acceptance testing**:

* The customer performs acceptance testing. They run test cases to see if the app
doesn't meet some of the requirenments in the contract. If it's unsuccessful,
they accept the app

##### __Some subtypes of the blackbox method__:

  * _Error guessing_

  * _Equialent partitioning_ (breaking input into few categories)

  * _Boundary-value analysis_ (test valid and invalid edges or input ranges)

  * _Cause-effect graphing_ (for each of the inputs create a graph to show how they
  are related to each other and their outputs)


##### __Some subtypes of the whitebox method__:
  
  * _Statement coverage_

  * _Decision coverage_

  * _Condition coverage_

  * _Multiple condition coverage_

#### Some hacks and technics for testing

* Test plan should include:
  1. objectives
  2. completion criteria
  3. schedules
  4. responsibilities
  5. libs and standarts
  6. tools
  7. computer time
  8. hardware configuration
  9. order of integration of the system parts
  10. tracking procedures
  11. debugging procedures
  12. regression changes (used for checking if changes affected other parts of the app)


* A necessary part of a test case is a definition of an expected result

* A completion criteria for the test cases: 

  * to estimate an overall number of errors

  * to find some percentage of them within the specified period of time

* If no errors have been found, evaluate the test cases

* It's useful to make a graph of the errors found since there's a rule -- if
there're lots of them discovered, there're still lots of them hiding

* Error analysis should be done in such way that such things get documented
and thought about:

  * who found the error

  * where it was found

  * what was the error

  * how should it have been prevented or detected earlier

* Create tables for test cases

#### Debugging

* There're few ways of debugging such as using print statement or using
debuggers vs debugging by examening how program works

* Use debugging tools as the last resort

#### Extreme programming

* XP is a programming paradigm focused on continuous integration, continuous testing,
pair programming, running unit tests, running acceptance tests, writing user stories

* XP propaganates writing unit tests before each module

#### Common things to test in web apps
  
  * ensure the application meets performance goals

  * verify that data is stored correctly

  * verify that you can recover using backups

##### *{{page.content | number_of_words}} words in the post*
