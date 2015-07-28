# Junit

failures vs Erros
 failures are when your test cases fail - i.e. your assertions are incorrect. 
 Errors are unexpected errors that occur while trying to actually run the test - exceptions, etc.
 
 
 @Before, @BeforeClass @After @AfterClass
 
 @Before
 In JUnit4 @Before is used to execute set of preconditions before executing a test.  For example, if there is a need to open some application and create a user before executing a test, then this annotation can be used for that method.  Method that is marked with @Before will be executed before executing every test in the class.
 
 @BeforeClass
 If a JUnit test case class contains lot of tests which all together need a method which sets up a precondition and that needs to be executed before executing the Test Case class then we can utilize “@BeforeClass” annotation. It is a static method. It  will be excuted only once. ex: to load the configuration file.
 
 @After
 Method that is marked with @After gets executed after execution of every test.  If we need to reset some variable after execution of every test then this annotation can be used with a method that has the needed code.
 
 @AfterClass
 n the same way “@AfterClass” annotation can be used to execute a method that needs to be executed after executing all the tests in a JUnit Test Case class. It is a static method. It  will be excuted only once. ex: to close the DB connections.


@Test
 This annotation is used to convert a normal method to a test method.
 @Test(expected = XX.class)
 @Test(timeout = xx)
 
@Ignore
 this method is not tested anymore.
 
@RunWith

1. @RunWith(Suite.class)  JUnit will invoke the class it references to run the tests in that class instead of the runner built into JUnit
2. @SuiteClasses({Task1.class,Task2.class,Task3.class})   all the tasks are as array
Suite is used to do the test classes together.


@Parameters

1. convert the default runner into @RunWith(Parameterized.class)
2. declare fields to store expected value and the test value.
3. declare a public static method whose return type is collection, with annotation @Parameters
4. declare a public constructor with all the parameters.


