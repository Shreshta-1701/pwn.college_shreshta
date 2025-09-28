# Multiple Globs
The challenge asks you to open the terminal in the pwn.college DOJO and use multiple globs at once to execute the run command with the correct argument and get the flag.

## My Solve
**Flag:** `pwn.college{UsIKTzUSfj3gJj527T3K28_Lce1.0lM3kjNxwCMxAzNzEzW}`

In this challenge, we use multiple globs in one argument. Let's take the example `/*fl*`. Here, the shell looks for all files within the `/` (root) directory that start with **anything**, then have **fl**, and end with **anything**, hence the `*` in the beginning and the end. IN this question, following the conditions given, we cd into `/challenge/files`, and then execute `/challenge/run *p*` to open the file that starts with anything, has the letter p, and then ends with anything. This gives us the flag.


```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{UsIKTzUSfj3gJj527T3K28_Lce1.0lM3kjNxwCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt how we can use multiple globs at once in one singular argument.

## References
None.