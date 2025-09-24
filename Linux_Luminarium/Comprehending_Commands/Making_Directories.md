# Making Directories
The challenge asks you to open the terminal in the pwn.college DOJO and create a directory and a file within it, before invoking the `run` program to find the flag.

## My Solve
**Flag:** `pwn.college{8XK0CDdR1-uw6F3cKh5RlRxvCOC.QXxMDO0wCMxAzNzEzW}`

The `mkdir` (make directory) command in Linux can be used to create directories (folders). This file takes one type of argument, that being, the path of where the new directory is to be located. If, instead of writing the whole path, we only mention the name of the directory to be made, then the command assumes that you wish to make the new directory inside the `cwd` of the terminal process. It is extremely similar to the `touch` command, the only difference between them being that `touch` creates files, whereas `mkdir` creates directories. In this challenge, we first have to make a `pwn` directory within `/tmp`, for which we can run `mkdir /tmp/pwn`. Then we must create a `college` file within the newly created directory. For this we enter `touch /tmp/pwn/college`. After this we can invoke `/challenge/run` to get the flag.

```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{8XK0CDdR1-uw6F3cKh5RlRxvCOC.QXxMDO0wCMxAzNzEzW}
```

## What I Learned
I learnt how we can make directories in Linux, which can be done with the help of the `mkdir` command, in a similar way as to how the `touch` command creates files. They even take the same type of arguments, only the `mkdir` command takes the names of the directories to be made instead of the files. 

## References
None.
