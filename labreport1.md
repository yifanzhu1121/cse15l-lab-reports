## Lab Report 1
> *Remote Access and FileSystem (Week 1)*

***Basic filesystem commands***:

**cd**: 
> "Change Directory" Used to switch the current working directory
1. With no arguments
   
   Command:
   ```
   # Example for cd command
   # No arguments
   cd
   ```
   Output (running in the directory where the command started):
   * No output.
   * It typically means the command executed successfully when there is no output.
   * The user is returned to `/home`.
   
2. With a path to a directory

   Command:
   ```
   # Example for cd command
   # A path to a directory
   cd lecture1
   ```  
   Output (running in the directory where the command started):
   * No output.
   * It typically means the command executed successfully when there is no output.
   * The user is directed to `/home/lecture1`.
  
3. With a path to a file

   Command:
   ```
   # Example for cd command
   # A path to a file
   cd en-us.txt
   ```
   Output (running in the directory where the command started):
   * It returns an error. 
   * The user cannot be directed to `/home/lecture1/messages/en-us.txt`, because `cd` is used to switch the directories but not files. 

  
**ls**:
> "List" Used to list the files and folders the given path
1. With no arguments
   
   Command:
   ```
   # Example for ls command
   # No arguments
   ls
   ```
   Output (running in the directory where the command started):
   * It prints out all the files and folders inside the current directory.

   Output 1 (running in the home directory `/home`):
   * `lecture1`
   * It prints out all the files and folders inside `/home`.

   Output 2 (running in the directory `/home/lecture1`):
   * `Hello.class  Hello.java  messages  README`
   * It prints out all the files and folders inside `/home/lecture1`.

   Output 3 (running in the directory `/home/lecture1/messages`):
   * `en-us.txt  es-mx.txt  ko.txt  zh-cn.txt`
   * It prints out all the files and folders inside `/home/lecture1/messages`.
   
2. With a path to a directory

   Command:
   ```
   # Example for ls command
   # A path to a directory
   ls lecture1
   ```  
   Output (running in the given directory `/home/lecture1`):
   * `Hello.class  Hello.java  messages  README`
   * It prints out all the files and folders inside `/home/lecture1`.
  
3. With a path to a file

   Command:
   ```
   # Example for ls command
   # A path to a file
   ls en-us.txt
   ```
   Output (running in the directory `/home/lecture1/messages`):
   * `en-us.txt`
   * It repeats the filename of the specified file `en-us.txt` and any requested information if given. 

**cat**:
> "Concatenate" Used to print the contents of one or more files given by the paths
1. With no arguments
   
   Command:
   ```
   # Example for cat command
   # No arguments
   cat
   ```
   Output (running in the directory where the command started):
   * It returns an error.
   * `cat` requires a file argument to display its contents. There is nothing to print out when no filename is given. 
     
2. With a path to a directory

   Command:
   ```
   # Example for cat command
   # A path to a directory
   cat lecture1
   ```
   Output (running in the home directory `/home`):
   * `cat: lecture1: Is a directory`
   * It returns an error.
   * `cat` requires a file argument to display its contents. There is nothing to print out when just a directory is given. 
  
3. With a path to a file

   Command:
   ```
   # Example for cat command
   # A path to a file
   cat en-us.txt
   ```
   Output (running in the directory `/home/lecture1/messages`):
   * `Hello World!`
   * `cat` displays the contents in the given file `/home/lecture1/messages/en-us.txt`.
