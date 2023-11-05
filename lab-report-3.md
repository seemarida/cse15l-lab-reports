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

## Part 2  
**grep command**  
1. ```grep -E "chain" 1471-2091-2-10.txt```  
part of the output:  
          ```chains. Distinct CD98 light chains appear to mediate
          heterodimer consisting of an 85 kD heavy chain and a 35
          kD light chain.
          with specific recognition of the CD98 heavy chain. Flow
          cytometry of CHO cells transfected with CD98 heavy chain
          cDNA confirmed that the CD98 heavy chain is the 6B12
          CD98 heavy chain was re-precipitated from an α3β1
          with CD98 (in the absence of manganese), the α chain must
          may reside in integrin α chain extracellular or```  
   I am searching for "chain" in the .txt file shown above, the output shows some of the lines from that text file that contain the term "chain". This is interesting because it allows you to quickly extract the information that you need rather than manually searching a large file.  
2. ```grep -c chain biomed```  
output:
```grep: biomed: Is a directory```
```0```
Using this command option is useful when you want to get a quick summary or a statistic about a frequently occuring pattern in your text file. This is interesting because it helps you quickly count the number of lines that correspond to a pattern, without outputing the actual lines, just the count.
3. ```grep -l chain 1471-2091-2-10.txt```
output:
```1471-2091-2-10.txt```
This command helps us quickly identify files that contain a keyword like "chain" in them. This is interesting because it shows us a list of filenames only and hides the matching lines.
4. ```grep -v chain 1471-2091-2-10.txt```  
some of the output:  
        ```Background
        The CD98 (4F2, FRP-1) molecule, a cell surface
        disulfide-linked heterodimer, was originally described as a
        T cell activation antigen [ 1 ] , and later was shown to
        provide a co-stimulatory signal for CD3-mediated T-cell
        activation [ 2 ] , independent of CD28/CD80/CD86
        interaction [ 3 ] . In other studies, triggering of human
        monocyte CD98 could suppress T cell proliferation [ 4 ] ,
        or promote homotypic cell aggregation of monocytes [ 5 ] .
        Also, CD98 may be a target antigen for natural killer cells
        [ 6 ] , may mediate fusion of blood monocytes leading to
        osteoclast formation [ 7 8 ] , and may modulate
        hematopoietic cell survival and differentiation [ 9 ] .
        The CD98 molecule is also widely expressed on rapidly
        growing non-hematopoietic cells, where it may modulate
        oncogenic transformation [ 10 11 ] , metal ion transport [
        12 13 ] , cell fusion [ 14 15 ] , and amino acid transport
        [ 16 17 18 19 ].```  
   This helps us indentify things like errors in a hypothetical data set, and helps clean your data in order to focus on relevant content, it does this by displaying all lines that do not contain the specified pattern we passed, then filters out the lines that match the pattern adn shows everthing else.
   


