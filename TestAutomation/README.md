
# Gherkin Test Scripts

Topics/Questions:
* What is Gherkin Syntax?
* Why use them / What are they for
* How do we write Gherkin test scenarios?

Discussion items:
* Define flows / patterns
* Create scripts (Jira features & test outcomes)
* Cypress integration

# What are they?

A set of grammar rules for defining feature flows in human-readable plain text that can be easily parsed with code.

> connects the human concept of cause and effect to the software concept of input/process/output.

Overview: https://cucumber.io/docs/guides/overview/

Key Points:
 - Behavior Driven Development
 - Structured Feature Definitions
 - Living Documentation
 - Executable Specifications

Example:
```gherkin
Scenario: Breaker guesses a word
  Given the Maker has chosen a word
  When the Breaker makes a guess
  Then the Maker is asked to score
```
Syntax
```gherkin
Feature: Title of the Scenario
Given [Preconditions or Initial Context]
When [Event or Trigger]
Then [Expected output]
```

References / More info:
https://www.guru99.com/gherkin-test-cucumber.html

## Practitest
https://www.practitest.com/qa-learningcenter/best-practices/bdd-testing/
![enter image description here](https://www.practitest.com/assets/img/learning-center/new-requirementBDD.webp)

## Cypress Integration:
https://www.npmjs.com/package/cypress-cucumber-preprocessor
```
import { Given } from "cypress-cucumber-preprocessor/steps";

const url = 'https://google.com'
Given('I open Google page', () => {
  cy.visit(url)
})
```

## Features:

Input Tables for validation different inputs
```
Scenario Outline: Add two numbers
Given I have entered <First> in the calculator
And I have entered <Second> into the calculator
When I press add
Then the result should be <Result> on the screen

Examples:
    | First | Second | Result |
    | 50    | 70     | 120    |
    | 30    | 40     | 70     |
    | 60    | 30     | 90     |
```

## 
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMTk4NDg1NDcsLTE1Mzc1NzQ1MjcsMT
E5MDQ3NTg2Nyw2MTg4OTE2NzcsMTc3MjExODIwMiwtNjgxODkw
MTk1XX0=
-->