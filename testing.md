## Testing Questions

* What are some advantages/disadvantages to testing your code?

+ Problems are discovered early.
+ Integration testing is easier.
+ Acts as documentation of the system.
+ Extremely accurate unit test coverage.
+ The unit test itself is used to verify the design.

+ Time consuming.
+ Does not show absence of errors.
+ Hard to set up realistic, useful tests.
+ Integration errors or system errors can be missed.
+ May be necessary to use a version control system.
+ Need to have a review process for test case failures.
+ Test program cannot be run in actual deployment environment.
+ Test code is likely to be at least as buggy as the code it is testing.
+ Value and accuracy of unit tests can be diminished if initial conditions are not set correctly.

* What tools would you use to test your code's functionality?

+ Mocha, chai, jasmine, karma

* What is the difference between a unit test and a functional/integration test?

+ Integration testing is when you test more than one component and how they function together. For instance how another system interacts with your system or the database interacts with your data abstraction layer. Usually this requires an fully installed system, although in its purest forms it does not.

+ Functional testing is when you test the system against the functional requirements of the product. Product/Project management usually writes these up and QA formalizes the process of what a user should see and experience, and what the end result of those processes should be. Depending on the product this can be automated or not.

* What is the purpose of a code style linting tool?

+ Linting is the process of running a program that will analyse code for potential errors.

* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

+ End-to-end testing is a methodology used to test whether the flow of an application is performing as designed from start to finish. The purpose of carrying out end-to-end tests is to identify system dependencies and to ensure that the right information is passed between various system components and systems.

+ (https://docs.angularjs.org/guide/e2e-testing)