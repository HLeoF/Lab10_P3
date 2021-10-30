Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?

	In my opinion, logger.log can record login information in text format.
	When we have problems when logging in, we can always check the log. The console log is used on the runtime, and it will only output the information of the logger in the console.
	It also can not store information. 

1.  Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
	
	It comes from the ConditionEvaluationResult. According to this error message.
	It tells us that this test is enabled because the disabled are not present.

1.  What does Assertions.assertThrows do?
	
	It catches an exception we specified. If the specified exception is caught, the test is passed. 
	However, if no exception is caught or the type of exception is incorrect, the test is failed.

1.  See TimerException and there are 3 questions
    1.  What is serialVersionUID and why do we need it? (please read on Internet)
	
	 The serialVersionUID is the serialization at runtime associates with each serializable class a version number.
	 We need it because serialVersionUID is used to ensure that during deserialization the same class is loaded.

    2.  Why do we need to override constructors?

    	 In my opinion, the TimerException can throw the error messages which tell us what the error is. 

    3.  Why we did not override other Exception methods?
    
    	 In my opinion, the TimerException not only can throw the error message, but it also tells us 
	 the reason that causes the error message to exist.

1.  The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
	  
	 The static block static {} is a static initializer. It is executed at class load initialization.

1.  What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)

	 The README.md file is a text file that introduces and explains the project, usually containing information about the project content.
	 It is an essential file for Bitbucket. It guides your users a quick understanding of how to install, use, and work with you.

1.  Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
	 
	 In the Timer class, it should be thrown TimerException when the timeToWait is equal to -1. 
	 The TimerEcception is work. However, when process into finally. two logger.info catch by
	 NullPointerException. logger.info should be not equal to null. It catches wrong information.

	 
1.  What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
	
	TimerException,
	Exception,
	NullPointerException --- for the two logger.info should not null, but the NullPointerException catch the 
	it as null. 
	RuntimeException,
	Exception

1.  Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel) 
1.  Make a printScreen of your eclipse Maven test run, with console
1.  What category of Exceptions is TimerException and what is NullPointerException

	The TimerException is cxception class ?
	The NullPointerException is a runtime exception

1.  Push the updated/fixed source code to your own repository.
