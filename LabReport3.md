# Lab Report 3

**Part 1:**

A failure-inducing input for the buggy program:

```
@Test
public void testReverseInPlace2() {
    int[] input1 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
}
```

An input that doesn't induce a failure:

 ```
 @Test 
public void testReverseInPlace3() {
	int[] input1 = { 1, 2, 1 };
	ArrayExamples.reverseInPlace(input1);
	assertArrayEquals(new int[]{1, 2, 1 }, input1);
}
```

 The symptom, as the output of running the tests:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/Screenshot%202024-02-12%20132011.jpg?raw=true)


 Code before fixing the bug:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```

 Code after fixing the bug:

```
static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      temp[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < arr.length; i += 1) {
      arr[i] = temp[i];
    }
  }
```

Why the code adjustment fixed the bug:
During the for loop of the original code for reverseInPlace, the element at the start of the list would get overwritted by the last element of that same list. To fix this I added a temporary array that would copy the elements from the original array into the new temporary array in reverse order, once the whole list is copied we now copy the temporary array back over to the original array in order to not overwrite the elements at the start.

---

**Part 2:**
