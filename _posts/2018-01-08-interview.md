---
layout: post
author: Joeny Bui
---

# Interview

## Five Steps a Technical Questions

1. Ask your interviewer questions to resolve ambiguity.

* What are the data types?
* How much data is there?
* What assumptions do you need to solve the problem.

2. Design an Algorithm

* What are the space and time complexities?
* What happens if there is a lot of data?
* Does your design cause other issues?
* If there are other issues, did you make the right trade-offs?
* If they gave you specific data, have you leveraged that information? 

3. Write pseudo-code first (but tell them).

4. Write your code, not too slow and not too fast.

* Use **Data Structures Generously**
* Write your code in the upper left hand corner to not crowd.

5. Test your code and *carefully* fix any mistakes.

* Extreme cases: 0, negative, null, maximums, etc
* User error: What happens if the user passes in null or a negative value?
* General cases: Test the normal case
* Testing while coding if it's hard code (bit shifting, arithmetic, etc)

## Five Algorithm Approaches

### Approach I: Examplify

Write out specific examples of the problem, and see if you can figure out a general rule.

### Approach II: Pattern Matching

Consider what problems the algorithm is similar to, and figre out if you can modifying the solution to develop an algorithm for this problem.

### Approach III: Simplify & Generalize

Change a constraint (data type, size, etc) to simplify the problem.  Then try to solve it.  Once you have an algorithm for the "simplified" problem, generalize the problem again.

### Approach IV: Base Case and Build

Solve the algorithm first for a base case (e.g. just one element).  Then, try to solve it for elements one and two.

### Approach V: Data Structure Brainstrom

This is hacky, but it often works.  Simply run through a list of data structures and try to apply each one.
