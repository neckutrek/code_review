# Code Review - Best Practices
Thoughts on best practices for code review

## Hot vs Cold Code Reviews
In a hot code review, 

## Code Comments
Comments in code should be seen as accompanying the code, not the other way around.
When doing a code review, leave the revireweing of comments to the latest.
First make sure that the code does what it should and then review the comments.

- In general, the necessity for comments implies that the code itself is not readable enough. When reviewing comments, look for deficiencies in code readability first.
- Don't comment file version changes! That information belongs in the file history in the version control system.
- If the implementation relies on a mathematical formulation, or some other external formulation, then the formulation should be documented in the code as comments, or should be refered to in the comments.

## Exception-Safety
Exception-safety is an important property of your code. 

- Destructors and overloads of operator delete and delete[] should NEVER throw. Make sure functions called also don't throw!

## Thread-safety

## Following SOLID principles

## Other guiding rules to follow
- Composition over inheritence

