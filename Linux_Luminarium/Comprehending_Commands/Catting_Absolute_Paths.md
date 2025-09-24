# Catting Absolute Paths
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the cat command to read the flag file, but this time with an absolute path.

## My Solve
**Flag:** `pwn.college{UqdL4Q0giVRP5mzqUW0dMvTRxOB.QX5ETO0wCMxAzNzEzW}`

The `cat` command can also involve absolute paths in its arguments. Here, we can use `cat /flag` to ask the cat command to read the flag file, and we have provided the process with the absolute path of the flag file.

```
hacker@commands~catting-absolute-paths:~$ cat /flag 
pwn.college{UqdL4Q0giVRP5mzqUW0dMvTRxOB.QX5ETO0wCMxAzNzEzW}
```

## What I Learned
I was able to learn more about the `cat` command and it's possible arguments, and how we can use absolute paths with the command to get rid of the need for relative paths.

## References
None.