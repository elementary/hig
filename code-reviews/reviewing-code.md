# Reviewing Code

## Partial is better than none

A partial review is better than no review: You don't need to fully understand the codebase to test its functionality. Often the feedback provided by a partial review helps to keep the momentum and multiple partial reviews eventually lead to a full review.

## Stay curious

If there's code you don't understand, ask about what it does. The chances are good it either needs a comment, could be refactored or you get to learn something new!

## Watch out for potential ways the code could fail

Because of Murphy's law ("Anything that can go wrong will go wrong") we want to make extra sure to keep an eye on potential pitfalls during code review. This is especially true for code that is responsible for carrying out a user's intent. Code which fails to execute a user initiated action _and_ is unable to inform the user about the error leads to a bad user experience.

## Recognize the good things

If you come across something you like about a proposed change, don't hesitate to let the developer know. Its just more fun to work with people who recognize the effort made.