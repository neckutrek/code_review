# Code Review - Best Practices
Thoughts on best practices for code review

## Size of each code review
Generally a code review is being made before committing a code change.


## Hot vs Cold Code Reviews
In a hot code review, 

Cold code review, 

## Code style
Does the code change adhere to the code style of the code base?
Spaces instead of tabs.
No trailing whitespaces.
No too long single code lines.
Readable function definition headers.

## Compile-time stuff
- Forward declarations over includes, this is to reduce compilation times.


## Code Comments
Comments in code should be seen as accompanying the code, not the other way around.
When doing a code review, leave the revireweing of comments to the latest.
First make sure that the code does what it should and then review the comments.

- In general, the necessity for comments implies that the code itself is not readable enough. When reviewing comments, look for deficiencies in code readability first.
- Don't comment file version changes! That information belongs in the file history in the version control system.
- If the implementation relies on a mathematical formulation, or some other external formulation, then the formulation should be documented in the code as comments, or should be refered to in the comments.

## Exception-Safety
Exception-safety is an important property of your code. It makes your code more robust to changes.

- Destructors and overloads of operator delete and delete[] should NEVER throw. Make sure functions called also don't throw!
- Exception-neutrality: all exceptions thrown should be either handeled locally, or be rethrown to client code to be handeled by the client code.
- Exception-safety: non-, basic, strong.

## Thread-safety
The C++ memory model is multi-threaded since C++11. When designing a public interface thread-safety has to be considered.

## Constexpr and templatization
- Can parts of the code change be made constexpr? This will make it more extensible as it can be used at compile time as well.
What part of the code can be made constexpr?

## Following SOLID principles
- Single responsibility. This applies to all modules, classes, and functions. Therefore, check for it on the module level, as well as on the class and per function level!
- Open/Closed principle. Is the modules and class
- Liskov substitution. subclass IS-A/WORKS-LIKE-A parentclass. I.e. the single responsibility principle should pertain throughout the inheritence tree. What to check for: if the parent class models a generalization of its subclasses.
- Interface segregation: 

## Optimization
Optimizing code is generally done at these different levels: at the system design level, at the program achritectural level, at the algorithm/data structure level, and at the final instruction level in respect to the target architecture.
- Does the design follow general system design principles set up for the project?
- Does the change 

## Testability


## Memory leaks


## Other guiding rules to follow
- Composition over inheritence

