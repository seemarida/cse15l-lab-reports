# Lab Report 3  
## Part 1  
**A failure-inducing input for the buggy program, as a JUnit test and any associated code**  
  ```
  @Test
  public void testReversed() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{1, 2, 3}, ArrayExamples.reversed(input1));
  }
```
**An input that doesn’t induce a failure, as a JUnit test and any associated code**  
```
@Test
  public void testReversedEven() {
    int[] input1 = {2,4,6,8};
    assertArrayEquals(new int[]{8,6,4,2}, ArrayExamples.reversed(input1));
  }
```
**The symptom, as the output of running the tests**  
<img width="599" alt="Screen Shot 2023-11-05 at 1 28 30 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/a44bb4ca-bb71-4f5c-a936-93c58d48da90"><img width="663" alt="Screen Shot 2023-11-05 at 1 29 15 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/6dd53edd-8f07-4893-9f9e-c0da3c49285b">  
**The bug, as the before-and-after code change required to fix it:**  
a) before  
<img width="385" alt="Screen Shot 2023-11-05 at 1 31 19 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/80e16b99-e1df-4805-85d3-2dac6bd62dec">

b) after  
<img width="411" alt="Screen Shot 2023-11-05 at 1 32 21 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/33bab948-8d7a-45f6-b306-20a186ba0641">  
**Briefly describe why the fix addresses the issue:**  
To fix this bug, I adjusted the for loop by changing i < arr.length to i < arr.length / 2. The reason this fix worked, is that it prevented the array from being reversed twice, therefore giving the proper output.  
