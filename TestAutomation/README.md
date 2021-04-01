
# Gherkin Test Scripts

Topics/Questions:
•	What is Gherkin Syntax?
•	Why use them / What are they for
•	How do we write Gherkin test scenarios?
•	Discussion items:
o	Define flows / patterns
o	Create scripts (Jira features & test outcomes)
o	Cypress integration

# What are they?

 - Behavior Driven Development

```gherkin
Feature: Title of the Scenario
Given [Preconditions or Initial Context]
When [Event or Trigger]
Then [Expected output]
```

```gherkin
Scenario: Breaker guesses a word
  Given the Maker has chosen a word
  When the Breaker makes a guess
  Then the Maker is asked to score
```

## Cypress Integration:


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMjQ1MzU3NDddfQ==
-->