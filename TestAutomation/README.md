
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
> Gherkin is a set of grammar rules that makes plain text structured enough for Cucumber to understand. The scenario above is written in Gherkin.

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
eyJoaXN0b3J5IjpbLTE1NzAxNzQyMjksNjE4ODkxNjc3LDE3Nz
IxMTgyMDIsLTY4MTg5MDE5NV19
-->