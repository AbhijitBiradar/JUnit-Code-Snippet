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
