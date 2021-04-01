
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

## Cypress Integration:
https://www.npmjs.com/package/cypress-cucumber-preprocessor
```
import { Given } from "cypress-cucumber-preprocessor/steps";

const url = 'https://google.com'
Given('I open Google page', () => {
  cy.visit(url)
})
```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5MDQ3NTg2Nyw2MTg4OTE2NzcsMTc3Mj
ExODIwMiwtNjgxODkwMTk1XX0=
-->