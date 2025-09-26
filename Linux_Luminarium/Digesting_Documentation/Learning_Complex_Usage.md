# Learning From Documentation
The challenge asks you to open the terminal in the pwn.college DOJO and read the flag file using an argument listed in the documentation.

## My Solve
**Flag:** `pwn.college{kwnDUJ6DuH49_FktYPA2KbqJtW2.QX1ITO0wCMxAzNzEzW}`

The challenge helps us further practice how we can use documentation to learn about new arguments and how we can put them to use. The documentation for this challenge states, that for example, running `/challenge/challenge --printfile /challenge/DESCRIPTION.md` prints out the Description file from the challenge directory. Over here, `--printfile` is an argument of the `/challenge/challenge` commands which prints out the file located at the path specified after the argument. If we want to read the flag file, then we must execute the command, `/challenge/challenge --printfile /flag` which will print out the contents of the file and give us the flag.


```
hhacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{kwnDUJ6DuH49_FktYPA2KbqJtW2.QX1ITO0wCMxAzNzEzW}
```


## What I Learned
I was able to further apply my knowledge of how we can use documentation to our advantage and use an argument listed in the documentation for the `/challenge/challenge` command in order to get the flag.

## References
None.