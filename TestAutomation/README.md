
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

Overview: https://cucumber.io/docs/gherkin/reference/

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
Scenario: Title of the Scenario
	Given [Preconditions or Initial Context]
	When [Event or Trigger]
	Then [Expected output]
```

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

Example inputs for validation across an input range
```gherkin
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

Different flows for a feature

```gherkin
Feature: Guess the word

  # The first example has two steps
  Scenario: Maker starts a game
    When the Maker starts a game
    Then the Maker waits for a Breaker to join

  # The second example has three steps
  Scenario: Breaker joins a game
    Given the Maker has started a game with the word "silky"
    When the Breaker joins the Maker's game
    Then the Breaker must guess a word with 5 characters
```

## Example for SCO


## Tools and References

https://cucumber.io/living-documentation/
https://www.guru99.com/gherkin-test-cucumber.html
https://cucumber.io/docs/guides/overview/

https://www.picklesdoc.com/pickles/Output/Dhtml/Index.html?feature=Features\00BasicGherkin\BasicGherkin.feature

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM2MDI5ODgyOSwyMDg0NDg5OTQwLC0xNT
M3NTc0NTI3LDExOTA0NzU4NjcsNjE4ODkxNjc3LDE3NzIxMTgy
MDIsLTY4MTg5MDE5NV19
-->