# Lab Report 5  
## Part 1: Debugging Scenario
**EdStem Post**  
My tests are failing, and I'm not sure why. Every time I try running ListExamples.java it seems like merge isn't working properly, because it's missing some elements. Here's my merge function:  

<img width="670" alt="Screen Shot 2023-12-03 at 4 20 00 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/7798d304-a05c-45c9-99db-0bbb1c0495e7">  

And here's the output for the tests:  

<img width="948" alt="Screen Shot 2023-12-03 at 4 19 15 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/4db744c7-7b2d-4aac-9f27-8c3ab9cd2b24">  

I can't seem to figure it out.  

**TA Response**  
To understand what's happening when the merge function is run, try to add print statements in your code, print out index1 and index 2 to ensure they're working currently, and go from there!  

**Student Response**  
Okay! I just added a few print statements to track the indices as well as print the final merged list.  

<img width="901" alt="Screen Shot 2023-12-03 at 4 32 54 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/58d1a79b-abf5-40ed-83b9-41cc914cdaa6">  

This was my output:  

<img width="1019" alt="Screen Shot 2023-12-03 at 4 34 34 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/a86a4a15-1952-4403-bcd5-644d2a575452">  

I noticed that after the first loop index2 was 2, but index1 was 0. I guess I forgot to increment index2, and so the last element in list2 kept getting skipped!  

<img width="312" alt="Screen Shot 2023-12-03 at 4 36 24 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/6a68cd13-1618-4881-89b7-b0dab837293a">  

Just ran my tests again, and it finally worked, thanks for your help!  

<img width="453" alt="Screen Shot 2023-12-03 at 4 37 12 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/7fe3b812-7658-4f4a-bf9f-7cdc7f5a0010">  

**Setup**  
- The file & directory structure needed
```
  *lab7  
    *ListExamples.java  
    *ListExamplesTests.java  
    *test.sh
```

  
- The contents of each file before fixing the bug
  
  <img width="344" alt="Screen Shot 2023-12-03 at 4 42 27 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/b959d1a3-ea6b-47eb-a3e2-36795d4cef89">  
  
- The full command line (or lines) you ran to trigger the bug
  
  `bash test.sh`  
  
- A description of what to edit to fix the bug
  
  Add `index2 +=1` to the merge function in the second while loop in the ListExamples.java file. Run `bash test.sh` once more.  

## Part 2: Reflection  
This course taught me so many things. I finally feel like I can easily set up my coding environment, which was something I struggled with in other CSE classes. I never thought I could actually *enjoy* using tools like Vim, for example, once the first half of the quarter passed, I started to find things more fun. The practical and applicable nature of the assignments, combined with the course's manageable workload is what allowed me to learn. I can't pinpoint what specific technical skills I learned, but I will say that this course has helped me out in terms of managing other CSE courses. Things like navigating a terminal and learning to use GitHub repositories became second nature. This type of efficiency in using these tools changed my perspective on the coding process. I went from being genuinely stressed out and overwhelmed by CS to being surprisingly comfortable and confident. This shift not only made me more productive but also made CS feel more approachable and less intimidating. I realized it's not just about writing code but about feeling at ease with the tools and processes that surround it.
