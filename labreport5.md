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

Thanks! I tried running `pwd` and `ls`, it does exist at the level. But upon reviewing my code, I realized the issue lies in how I'm specifying the path to the data directory. I assumed the working directory would be the project root `/home/user/myJavaProject`, but it turns out the working directory was actually set to the src directory where my Java file is located `/home/user/myJavaProject/src`.

![Image](1.png)

I modified the path to the `data` directory to account for the actual working directory by changing the path to `../data`, which is one level up from the current `src`. And now it lists the files in `data` without throwing error message.
