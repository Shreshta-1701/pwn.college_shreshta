# Comparing Files
The challenge asks you to open the terminal in the pwn.college DOJO and compare the contents of 2 files and find the difference between them, which would be the flag.

## My Solve
**Flag:** `pwn.college{IgaQjCmDrlZ0u9u_9nDmE0za5rZ.01MwMDOxwCMxAzNzEzW}`

In this challenge, we use the `diff` command. This command can be used to compare 2 files and print out the differences between them. This command can take multiple arguments, the arguments being the paths of the the files that we wish to compare. After comparing, the command prints out the lines which are different, or if there are more lines in one of the files, and then prints out the difference itself. In our case, since the second file has one extra line of text in between containing the flag, therefore the command prints `39a40` which means that there is an additional, different line in File 2 that comes after the 39th Line in File 1. This is our flag.

```
hacker@commands comparing-files:~$ diff /challenge/decoys_only.txt /challenge/dec oys_and_real.txt

39a40

> pwn.college{IgaQjCmDrlZ0u9u_9nDmE0za5rZ.01MwMDOxwCMxAzNzEzW}
```

## What I Learned
I was able to learn how we can use the `diff` command to compare files for differences and how to understand the output it gives us, which tells us which lines are different and in what way, and also prints out the different lines.

## References
None.