# The Root
The challenge asks you to open the terminal in the pwn.college DOJO and find the flag by accessing the `pwn` program.

## My Solve
**Flag:** `pwn.college{gdMvHfavLfP3S3XTzmBYdvJzSkz.QX4cTO0wCMxAzNzEzW}`

A terminal session always starts within the root directory. To take proper advantage of our Linux system, we need to learn how to access other sub-directories and programs. We can access the /pwn program (a program inside the root directory) which holds the flag for this challenge. To do so, we need to enter `/pwn` in the terminal to access the program to receive the flag.

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{gdMvHfavLfP3S3XTzmBYdvJzSkz.QX4cTO0wCMxAzNzEzW}
```
## What I Learned
I learnt about directories in Linux and how we can access programs in a directory. I also learnt what an `absolute path` is and how it is different from a relative path. An absolute path always starts from the root directory.

## References
None.
