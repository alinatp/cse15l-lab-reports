# Lab Report 2 - Servers and Bugs (Week 3)

## Part 1
The code for `String Server`

* Which methods in your code are called?
* What are the relevant arguments to those methods, and the values of any relevant fields of the class?
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

## Part 2
**Symptoms and Failure-inducing Inputs (Array Methods - `reverseInPlace`)**
Failure-inducing input
```
@Test
  public void testReverseInPlace2() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3, 2, 1}, input1);
  }
```

Input that doesn’t induce a failure
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```



Before Fix
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After Fix
```
 static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return arr;
  }
```

## Part 3
**What did I learn these past weeks?**
These past few weeks I learned about URls and servers. I now understand the different components that make up webservers like domain and path.
The domain being the part of the URL after the https:// and before the first slash. The path being the part after the domain and before the ?.
