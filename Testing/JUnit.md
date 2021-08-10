# JUnit

Using JUnit, you can write unit tests asserting results, meaning, you can compare an expected result with the actual one.

---
```@Test``` [[Annotation]]
```kts
@Test
fun testFunction() {

}

```
This tells JUnit that the method is a test.


## Common Assertions

##### assertEquals:
- the first parameter is the **expected value**, and the second parameter is the **actual value**.
```kts
val actual = 1 + 2
val expected = 3
Assert.assertEquals(expected, actual)
```
- There’s also the possibility to write a message so that, when the test fails, you’ll see this message.
```kts
val actual = 1 + 2
val expected = 3
Assert.assertEquals("Number should have been 3", expected, actual)
```



##### assertTrue:
- 
```kts
val expected = 3
Assert.assertTrue(actual == 3)
```


---
##### assertFalse:
	- 
```kts
val expected = 3
Assert.assertFalse(actual != 3)
```