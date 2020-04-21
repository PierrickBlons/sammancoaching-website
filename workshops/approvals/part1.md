---
layout: default
title: Approval Testing Intro
parent: Approval Testing
grand_parent: Workshops
nav_order: 1
---

# Introduction to Approval Testing

This first module goes through the main characteristics of Approval testing:

- Test cases check actual program output against a previously approved value, and any difference will fail the test.
- Normally, a human inspects and approves some actual program output when creating a test case.
- Raw program output may be processed into a more convenient format before being used for approval and comparison.
- Design a Printer to display complex objects, instead of many assertions.
- If actual program output is not yet available, the approved value may be a manual sketch of the expected output.
- Approved values are stored separately from the sourcecode for the test case, although in the same VCS repository.
- When a test case fails, you can use a tool to inspect the differences and easily update the approved value.

We work through some exercises and gain experience with the ['Approvals'](https://github.com/approvals) tool. We will work in small groups and each group can agree which programming language to use. The exercises are generally available in Java, C#, Python and C++.

## Session Outline
 
* 10 min connect: Approval Testing warm up questions 
* 10 min connect: Short introductions and form groups
* 15 min concept: Demo
* 30 min concrete: Do some approval testing
* 5 min conclusions: How about?

(short break)

* 5 min connect: Read through the How about? questions and add more you think of
* 10 min concept: Characteristics of Approval testing
* 10 min concrete: Update some existing tests
* 5 min concept: Approval testing detects both bugs and features
* 15 min concrete: Update tests making one change at a time
* 10 min conclusions: explain characteristics to someone else

(short break)

* 10 min connect: Situations where this won't work
* 10 min concept: Pre-comparison processing
* 20 min concrete: Do some pre-comparison processing
* 15 min concrete: Demo pre-comparison processing
* 10 min conclusions: Look again at the situations where this won't work

(short break)

* 5 min concept: Remaining characteristic - sketching
* 15 min concrete: demo of sketching a new test case
* 10 min conclusions: walkabout posters & code review
* 15 min retrospective: gather observations

## Part 1

### Connect - Warm up Questions

Look at these [warm-up questions](../../exercises/warm_up_questions/approval_testing_warm_up_questions.html). Think for yourself then discuss with a pair.

### Connect - Introduce and form groups

Organize people into groups of 2-3 where they can agree on a programming language. Mix up people from different companies.

### Concept - Demo of Approval testing

Show converting the first test for [Supermarket Receipt](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata) into an approval test.

After the demo - get people to "Think and write" their first impressons

* Think about what you just saw. If you had to explain the main idea to someone else, what would you say?
* Write your explanation in a sentence or two.

### Concrete - Do some approval testing

Have them convert the first test for[Supermarket Receipt](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata) into an approval test, then write more tests for other kinds of discount.

### Conclusions - How about?

* On a sticky note, write a question you want answered about Approval Testing
* Stick it on the “How about?” board
* Take a break

## Part 2

### Concept - Characteristics of Approval testing

Go through the characteristics they should have come accross already. Answer the questions from the "How about" board if they are relevant here.

- Test cases check actual program output against a previously approved value, and any difference will fail the test.
- Normally, a human inspects and approves some actual program output when creating a test case.
- Design a Printer to display complex objects, instead of many assertions.
- Approved values are stored separately from the sourcecode for the test case, although in the same VCS repository.

Any remaining unanswered questions from the 'How about' board? Either handle them now or say in which module we'll answer them later.

### Concrete - update some existing tests

Practice using the diff tool to inspect differences and approve those that aren't bugs. Use the java version of [Supermarket Receipt](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata) on the 'with_broken_tests' branch.

### Concept - Approval testing detects both bugs and features

Additional characteristic we have come accross now:

- When a test case fails, you can use a tool to inspect the differences and update the approved value.

Explain what 'over-specified' tests are and why they could be bad.

### Concrete - Update tests making one change at a time

Use the java version of [Supermarket Receipt](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata) starting on the 'with_tests' branch. For each file in turn, look at a diff with the "with_broken_tests" branch.

* Product
* REceiptItem
* ReceiptPrinter
* ReceiptPrinterTest
* ShoppingCart
* ShoppingCartTest

Introduce these changes into your branch one at a time, in the order listed above. Update the tests as needed after each change.

### Conclusions - explain characteristics to someone else 

In small groups, take turns to explain the characteristics of approval testing. How does it change the way you work?

## Part 3

### Connect - Situations where this won't work

In small groups, look through these [Puzzles](https://github.com/emilybache/Approvals-Puzzles). Which ones could you test with approval testing? Which ones would be easier to test a different way?

### Concept - pre-comparison processing

This characteristic: 

- Raw program output may be processed into a more convenient format before being used for approval and comparison.

And to some extent this one:

- Design a Printer to display complex objects, instead of many assertions.


### Concrete - exercise with pre-comparison processing

Use the java version of [Supermarket Receipt](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata) starting on the 'with_date' branch. All the tests are currently failing. 

* Why are the tests failing?
* Come up with two or three strategies for how to make them pass again.
* Pick a strategy and implement it so the tests pass.

For bonus points, try to use a strategy that fixes the tests but doesn't alter the production code or the ReceiptPrinter or the approved files.

### Demo - pre-comparison processing

Demo solution to the previous exercise. Also demo solutions to these [Puzzles](https://github.com/emilybache/Approvals-Puzzles) using TextTest.

### Conclusions

Review your choices for the [Puzzles](https://github.com/emilybache/Approvals-Puzzles). Do you still make the same choices? Can you think of any more kinds of program output that would not be suitable for Approval testing?

## Part 4

### Concept - Sketching

- If actual program output is not yet available, the approved value may be a manual sketch of the expected output.

### Concrete: demo of sketching a new test case

Add Tax calculations to the receipt. Sketch it first.

### Conclusions: walkabout posters & code review

Get people to look through everything we've done today and discuss with someone what they've learnt.

### Retrospective: gather observations

Ask people to note down what has happened today in these categories:

* Liked
* Learned
* Lacked
* Longed for

