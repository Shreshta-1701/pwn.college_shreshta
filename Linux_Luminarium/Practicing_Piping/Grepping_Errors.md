# Grepping Errors
The challenge asks you to open the terminal in the pwn.college DOJO and grep through the errors of a command without creating an error file.

## My Solve
**Flag:** `pwn.college{sUWACYUzpobwzu1RZQrYe1NwOYR.QX1ATO0wCMxAzNzEzW}`

We can grep directly through a command's output by using the pipe operator, but this cannot be done with error files as the `|` operator does not take File Descriptors alongside it. What we can do however, is redirect the standard error to a standard output. Then, we can grep through the combined standard error and standard output by using the `|` operator. The syntax for this is `2> &1`. The command to be executed for this challenge, according to the conditions is `/challenge/run 2>& 1 | grep pwn.college`, which searches for the term **pwn.college** in the combined stderr and stdout file, and gives us the flag.


```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{sUWACYUzpobwzu1RZQrYe1NwOYR.QX1ATO0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I was able to learn how I can combine stderr and stdout in one, in order to grep through the errors of a command directly using the `|` or pipe operator.

## References
None.