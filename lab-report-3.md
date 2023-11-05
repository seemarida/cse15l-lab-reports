# Lab Report 3  
## Part 1  
A failure-inducing input for the buggy program, as a JUnit test and any associated code  
  ```
  @Test
  public void testReversed() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{1, 2, 3}, ArrayExamples.reversed(input1));
  }
```
An input that doesn’t induce a failure, as a JUnit test and any associated code  
```
@Test
  public void testReversedEven() {
    int[] input1 = {2,4,6,8};
    assertArrayEquals(new int[]{8,6,4,2}, ArrayExamples.reversed(input1));
  }
```
