# Redirecting Output
The challenge asks you to open the terminal in the pwn.college DOJO and redirect the output of a command to a file.

## My Solve
**Flag:** `pwn.college{ctwFGC2RwhDMweoKwjc0IE_cMRe.QX0YTN0wCMxAzNzEzW}`

In this challenge, we are tasked with redirecting the output of a command to another file. This can be done with the help of the `>` character, where the output to be redirected comes before the character, and the location where it is to be redirected comes after the `>` character. For example, here, we need to redirect the output of `echo PWN` to the file `COLLEGE`. So, we execute the command `echo PWN > COLLEGE`. This gives us the flag.


```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{ctwFGC2RwhDMweoKwjc0IE_cMRe.QX0YTN0wCMxAzNzEzW}
```


## What I Learned
I learnt how we can redirect the output of commands to a file using the `>` character. This is also known as redirecting `stdout` to files.

## References
None.