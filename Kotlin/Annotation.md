# Annotations



## Test Annotations
JUnit

Examples:
```kts
@Test
// This will tell JUnit that this method is a test.

@Before
// This method will be executed before each test 
// and it’s a good place to set up objects.
// Helps reduce boilerplate code

@After
// The method will be executed after each test. 
// You can use it to tear down anything or reset
// any objects that you set up in @Before.

@BeforeClass
// If you annotate a method with this, it’ll be 
// executed only once before all the tests are 
// executed. For example, opening a file, a 
// connection or a database that is shared in all 
// the tests.

@AfterClass
/*
Use this one to execute a method only once after 
all the tests are executed. For example, 
closing a file, a connection or a database that 
is shared in all the tests.
*/
```