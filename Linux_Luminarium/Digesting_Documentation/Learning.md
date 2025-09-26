# Learning From Documentation
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the challenge program with the correct argument.

## My Solve
**Flag:** `pwn.college{I8phYVWZLNVCzauRm3ULaLpXtST.QX0ITO0wCMxAzNzEzW}`

The challenge talks about how Documentation is extremely important for even figuring out what to do with each command. It tells us about the documentation for the /challenge/challenge command which invokes the challenge program to give us the flag. We learn that to get the flag, we must use the argument `--giveflag` along with the `/challenge/challenge` command.


```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{I8phYVWZLNVCzauRm3ULaLpXtST.QX0ITO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how we can use Documentation and learn from it in order to be able to use new commands properly, especially when we have just started out with linux.

## References
None.