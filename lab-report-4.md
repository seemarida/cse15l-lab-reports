# Lab Report 4  
## Step 1: Log into ieng6  
I first typed `ssh cs15lfa23mh@ieng6.ucsd.edu` to log into the remote server, then hit <enter>.  
<img width="697" alt="Screen Shot 2023-11-30 at 8 38 27 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/953a32ca-4fb8-481f-bb87-40732b37aa28">  

## Step 2: Clone your fork of the repository from your GitHub account (using the SSH URL)  
<ctrl+c> from GitHub to copy the SSH URL.  
<img width="1494" alt="Screen Shot 2023-12-02 at 6 03 26 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/030b0807-0e49-4e0d-9022-18dde08a6366">  
  
then typed `git clone` then hit <ctrl+v> to clone the URL, and hit <enter>.  
<img width="759" alt="Screen Shot 2023-12-02 at 6 04 59 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/2c0c4a43-d1ba-4c4c-9ce2-dbf6c36c5f33">  
  
## Step 3: Run the tests, demonstrating that they fail  
Typed `cd lab7` to go into the lab7 directory where the test script is located.  
<img width="724" alt="Screen Shot 2023-12-02 at 6 06 33 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/f8c31f8f-8d5e-4d07-bad7-1bbcf2f21411">  
  
then typed `bash t` <tab> then `.` so `bash test.sh` popped up, then hit <enter> to run the test script commands.  
<img width="741" alt="Screen Shot 2023-12-02 at 6 08 28 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/dd37edc6-6f4a-4c26-bc08-a7163bee5be5">  
  
## Step 4: Edit the code file ListExamples.java to fix the failing test  
typed `vim L` <tab> `.j` <tab> so that `vim ListExamples.java` pops up, then hit <enter>, to view the ListExamples.java file and look for the error I need to edit.  
<img width="585" alt="Screen Shot 2023-12-02 at 6 13 44 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/34b06cd4-fd50-482d-96ed-e8d41c4d5d59">  
  
in the Vim window, I typed `i` to go from normal mode to insert mode, < down > x43, < left > x7, < backspace >, then `2`, in order to change `index1` to `index2`  
<img width="549" alt="Screen Shot 2023-12-02 at 6 17 24 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/57a6cd2b-3dd9-4357-a541-2718785344cd">  
  
I then pressed <esc> to exit insert mode and go back to normal mode, then I typed `:wq` and <enter> to save my changes and exit Vim.  
  
## Step 5: Run the tests, demonstrating that they now succeed  
I just pressed <up> to get `bash test.sh` to show up then pressed <enter>, to compile and rerun ListExamplesTests.java.  
<img width="497" alt="Screen Shot 2023-12-02 at 6 21 50 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/a84fae9d-0195-44e7-95ed-f7fb91bdd559">  
  
## Step 6: Commit and push the resulting change to your GitHub account  
Finally, I typed `git commit -a -m “updated”` and <enter>which did a git add and commit within the same command and committed the changes to my GitHub account. Then I typed `git push` and <enter>, resulting in the message below.  
<img width="853" alt="Screen Shot 2023-12-02 at 6 24 13 PM" src="https://github.com/seemarida/cse15l-lab-reports/assets/121886487/bcaf59cc-a57e-427e-b546-7d4e8bb52554">  

