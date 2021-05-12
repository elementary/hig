---
description: How to make a Code Review a fruitful experience for coders and reviewers alike.
---

# Code Reviews

Code reviews play a crucial role in the elementary OS development process: Having other people verifying your code works as intended is certainly a big boost for overall code quality. But they serve an even bigger purpose: They provide the opportunity to learn from each other. This guide provides some tips and best practices to minimize the barriers for doing or receiving Code Reviews.

## Writing Code for Reviews

### Program for the present, not the future

At elementary we believe in the YAGNI principle (You aren't gonna need it): Always implement when you _actually have_ a need - but never when you _think_ you are _gonna_ need it. Combined with continous refactoring, the YAGNI principle keeps the code base as simple as possible and helps us to avoid technical debt.

### Avoid big changes in one go

As someone proposing a code change, probably the most helpful thing is to keep it small. A small Pull Request feels less intimidating for a code reviewer, so there is a highler chance to get timely feedback for such a request. In addition, a small change is a lot less to test and there is a much smaller chance of a regression - both things lead to a higher overall quality and therefore to a better experience for the end user.

If you're proposing large functional changes, it's usually better to propose clean ups in several smaller Pull Request and linking them to a corresponding Issue report which explains the overarching goal.

### Keep it self contained

It's really tempting to do a lot of refactoring as you see it, but this makes it really hard for a reviewer to understand the important parts for the functional changes.

### Keep it consistent

Naming is one of those things that feels trivial but really helps in a few years when it's all new eyes on some code. Especially if we can use names that sound like the ones already present in the libraries consumed it can make it much easier to figure out what's happening.

### Comment non-trivial code

If you are writing some non-trivial code, make sure to add a comment which explains exaclty what and more importantly why your code does what it does.

### Describe your change

Make sure you describe the changes you are proposing in the Pull Request description. If appropriate, add a screenshot or a short video to show case your change. This cuts down a lot on the time a reviewer needs to invest to understand your code.

### Review your Code yourself first

When you got your initial version for the poposed change working, look into the code you've added once again and ask yourself if anything could be done in a better fashion before
sending it to official Code Review. Of course, if you want some early opinion, there is always the possibility to open a Draft Pull Request as well.

## Doing Reviews

### Partial is better than perfect

A partial review or is better than no review: You don't need to fully understand the codebase to test its functionality. Often the provided feedback of a partial review helps to keep the momentum going and eventually leads to a full review.

### Stay curious

If there's code you don't understand, ask about what it does: The chances are good it either needs a comment, could be refactored or you get to learn something new!

### Watch out for potential ways the code could fail

Because of Murphy's law ("Anything that can go wrong will go wrong") we want to make extra sure to keep an eye on potential pitfalls during code review. This is especially true for
code that is responsible for carrying out a users intent: Code which fails to execute a user-initiated operation and is unable to inform the user about such an error leads to a bad user experience.

### Recognize the good things

If you come across something you like about a proposed change, don't hesitate to let the developer know. Its just more fun to work with people who recognize the effort made.