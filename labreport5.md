## Lab Report 4
> *Week 8 & Week 9*

<br />

**Original Post**: 

Hi everyone,

I'm having some trouble with my Java program which is designed to list the contents of a specified directory. Despite the directory existing and containing files, my program throws a `FileNotFoundException`. Here's the error message:

![Image](1.png)

I thought the problem might be with the directory path I'm providing, but I've double-checked and it seems correct. The program is supposed to list files from the data directory within the project folder, but it's not finding the directory for some reason.

Thanks for helping.

<br />

**TA Response**: 

Hi,

The `FileNotFoundException` could indeed suggest a path issue. Try running the `pwd` command to confirm the current working directory. Also, you could check the contents of your current directory. This will help us see if the data directory is in the expected location relative to where your program is running.

<br />

**Follow-up Post**: 

Thanks! I tried running the program with the absolute path, and the issue remained 
the same. And here's a screenshot of it and another one of the ls -l command output:

![Image](1.png)

It looks like the file is there, and the permissions seem fine. So the issue might 
be somewhere in how the program reads the file line by line. Maybe it's trying to open the file multiple times within a loop?
