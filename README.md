# JUnit

Q: JUnit Assertion

#1) assertEquals
String expected = “https://www.google.com”;
String actualURL= “https://www.google.com”;
Assert.assertEquals(expected, actualURL);

#2) assertTrue
Assert.assertTrue(“Assert True test message”, true);

#3) assertFalse
Assert.assertFalse(“Assert false test message” false);

#4) assertNull
DemoClass demo = new DemoClass();
Assert.assertNull(demo);

#5) assertNotNull
DemoClass demo = new DemoClass();
Assert.assertNotNull(demo);

#6) assertSame
DemoClass1 demo1 = new DemoClass1();
DemoClass2 demo2= new DemoClass2();
Assert.assertSame(“Two objects are equal”, demo1, demo2);

#7) assertNotSame
DemoClass1 demo1 = new DemoClass1();
DemoClass2 demo2= new DemoClass2();
Assert.assertNotSame(“Two objects are not equal”, demo1, demo2);

#8) assertArrayEquals
String[] expected = {“Mango”,”Apple”,”Banana”}
String[] actual = {“ Mango”,”Apple”,”Banana”}
Assert.assertArrayEquals(expected,actual);








Sample JUnit Test
public class Example {
	@BeforeClass
	public static void setup() {
	}

	@Before
	public void setupThis() {
	}

	@Test
	public void method() {
	org.junit.Assert.assertTrue(new ArrayList().isEmpty());
	}

	@After
	public void tearThis() {
	}

	@AfterClass
	public static void tear() {
	}
}


Assert Class

void assertEquals(boolean expected, boolean actual)
	Checks that two primitives/objects are equal.

void assertFalse(boolean condition)
	Checks that a condition is false.

void assertNotNull(Object object)
	Checks that an object isn't null.

void assertNull(Object object)
	Checks that an object is null.

void assertTrue(boolean condition)
	Checks that a condition is true.
	
void fail()
	Fails a test with no message.
	
	
	
Annotation

@Test
	The Test annotation tells JUnit that the public void method to which it is attached can be run as a test case.
	
@Before
	Several tests need similar objects created before they can run. Annotating a public void method with @Before causes that method to be run before each Test method.

@After
	If you allocate external resources in a Before method, you need to release them after the test runs. Annotating a public void method with @After causes that method to be run after the Test method.
	
@BeforeClass
	Annotating a public static void method with @BeforeClass causes it to be run once before any of the test methods in the class.

@AfterClass
	This will perform the method after all tests have finished. This can be used to perform clean-up activities.

@Ignore
	The Ignore annotation is used to ignore the test and that test will not be executed.


JUnit Annotation Execution Flow
in before class
in before
in test case 1
in after
in before
in test case 2
in after
in after class


JUnit Annotation Parameter
@Test(timeout = 1000)
@Test(expected = ArithmeticException.class)


Test Suites
 
@RunWith(Suite.class)
 
@Suite.SuiteClasses({
   TestJunit1.class,
   TestJunit2.class
})
 
public class JunitTestSuite {   
}  


Sample JUnit Test Runner

public class TestRunner {

	public static void main(String[] args) {
		//This result object has many methods and it is very useful
		//Type result and press dot, all the methods will display
		//This statement is to load all type of results in the result object
		Result result = JUnitCore.runClasses(JunitMathProvider_1.class);
		//Here it is getting the run count from the result object
		System.out.println("Total number of tests " + result.getRunCount());
		//This is to get the failure count from the result object
		System.out.println("Total number of tests failed " + result.getFailureCount());

		for(Failure failure : result.getFailures())
		{	
			//This will print message only in case of failure
			System.out.println(failure.getMessage());
		}
		//This will print the overall test result in boolean type
		System.out.println(result.wasSuccessful());

	}

}


Parameterize Test---Pending	
