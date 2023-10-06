# Lab Report 1

## 1. Share an example of using the command with no arguments.  


a)`cd`  


![Image](cd1.png)  
The working directory was /home before and after the command was run because it ran with no arguments and so there were no new directories it stayed in the same one. The output was not an error.  

  b)`ls`  
  
![Image](im.png)  
Similar to the previous example, /home is the working directory after running the command ls, the output is all the available directories inside in /home, in this case, it is only lecture1. The output was not an error.  

  c)`cat`  

![Image](cat1.png)  
This command does not output anything apparent, the working directory was /home and remained the same. There was nothing in the filesystem so cat was a useless command in this case. The output did not generate an error message, because it was reading the files but did not display anything.  

---  


## 2. Share an example of using the command with a path to a directory as an argument.  

   a)`cd`  
   
   
![Image](image.png)  

Running cd lecture1 will change the current directory from /home to /home/lecture1. The output is only a change in the directory and now you can access things within that new directory. The output was not an error.  

  b)`ls`  
  
   
![Image](im2.png)  

Running ls lecture1 shows us files inside of /home/lecture1. The current directory is /home/lecture1 since we specified it as an argument. The output is not an error.  


  c)`cat`  
  ![Image](cat2.png)  
  
Running cat lecture1, just shows us that lecture1 is indeed a file and confirms it by reading the files in the directory. The directory does not change when the command is run and is still /home. The output is not an error.  

---  


## 3. Share an example of using the command with a path to a file as an argument.  


   a)`cd`  
   
   
![Image](image2.png)  

cd is for changing directories, not opening files. So using a filename like Hello.java will result in a "directory not found" error. Running cd Hello.java does not change the directory if it is /home. The output is an error since Hello.java is not a directory that cd can go to.  

  b)`ls`  
  
![Image](im3.png)  

Running ls Hello.java does not change the directory /home. Output is an error because ls is used to list or view files in a directory, and not to display information about a file.  



  c)`cat`  
  
  ![Image](thirdcat.png)  
  
  
Running cat Hello.java has to change the directory to /home/lecture1 to display the code of Hello.java, you must specify what the path is before that. No errors in the output.  

