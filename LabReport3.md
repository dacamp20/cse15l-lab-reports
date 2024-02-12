# Lab Report 3

---

**Part 1:**

A failure-inducing input for the buggy program:

`@Test 
	public void testReverseInPlace2() {
    int[] input1 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
	}`

An input that doesn't induce a failure:

 `@Test 
	public void testReverseInPlace3() {
    int[] input1 = { 1, 2, 1 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1, 2, 1 }, input1);
	}`

 The symptom, as the output of running the tests:




 Code before the fixxed bug:

`
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
`

 Code after fixing bug:

`
static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      temp[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < arr.length; i += 1) {
      arr[i] = temp[i];
    }
  }
`
 
