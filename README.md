Tasks to answer in your own README.md that you submit on Canvas:

1. See logger.log, why is it different from the log to console?
   1. logger.log is different than the log to console since it displays the error as a FINER message.
2. Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
   1. The line comes from a call in void failOverTest() method.
3. What does Assertions.assertThrows do?
   1. It asserts that an executable block throws an exception.
4. See TimerException and there are 3 questions
    1. What is serialVersionUID and why do we need it? (please read on Internet)
       1. We use the serialVersionID to remember versions of a Serializable class to verify that a class and the Serializable class work together.
    2. Why do we need to override constructors?
       1. We override constructors to create new exception types that pertain specifically to our program.
       2. Exception constructors don't override their superclass' constructor, but they do call super().
       3. Subclasses do not inherit constructors from super class, but the constructor for the superclass is invoked by the subclass.
    3. Why we did not override other Exception methods?
       1. We don't override other Exception methods since they are inherited from the super class.
5. The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
   1. A static block is used each time  class is loaded into memory. It is useful for setting up static data or logging (would apply to every instance of the class).
6. What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
   1. A README.md file is a file using markdown language for formatting text. Bitbucket uses it for their Data Center and Server. 
7. Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
   1. The test is failing since timeNow is null when the time to wait is less than 0. It is throwing an uncaught NullPointerException.
8. What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
   1. The actual issue is that Exception gets thrown but there is nothing to catch it. JUNIT gets an assertion error and has no way to handle it.
9. Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel)
10. Make a printScreen of your eclipse Maven test run, with console
11. What category of Exceptions is TimerException and what is NullPointerException
    1. Both TimerException and NullPointerException are runtime errors.
12. Push the updated/fixed source code to your own repository.