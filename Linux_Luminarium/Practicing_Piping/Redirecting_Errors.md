# Redirecting Errors
The challenge asks you to open the terminal in the pwn.college DOJO and redirect the output of a command to a file and the errors to another file.

## My Solve
**Flag:** `pwn.college{wx0qJQPw0Y9JOlF4kxFkZHVE6AP.QX3YTN0wCMxAzNzEzW}`

This challenge introduces us to File Descriptors. These are something that we have been using for quite some time already, but the File Descriptors for Standard Output and Standard Input (0 and 1) don't need to be entered as they get added in by default, unless the File Descriptor for Standard Error is specified. By specifying this File Descriptor, we can redirect all errors produced by a command to a file. The syntax for this is `command 2> error_file`. For this challenge, we are tasked to redirect the output of `/challenge/run` to a file, and the errors of this command to another file. For this, we execute the command `/challenge/run > myflag 2> instructions`. After this, we can read myflag using `cat myflag` to get the flag.


```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{wx0qJQPw0Y9JOlF4kxFkZHVE6AP.QX3YTN0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt about File Descriptors and how I had actually already been using them. I learnt how to redirect errors from a command to a file, and also learnt how to redirect multiple parts of a command (output, errors) to different files all at the same time through one single statement.

## References
None.