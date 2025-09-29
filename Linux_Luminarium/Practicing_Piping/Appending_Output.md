# Appending Output
The challenge asks you to open the terminal in the pwn.college DOJO and append command output to a file.

## My Solve
**Flag:** `pwn.college{EY07vJn2tho-dFDOUjznHkhEu7W.QX3ATO0wCMxAzNzEzW}`

Redirection of output is done usually so that command outputs can be stored in files for later use. The most convenient way to do this being to store command outputs of multiple commands all in file, and grepping through it later on when we need a specific output. However, the `>` character deletes the previous contents of the output file and creates a new one every time, and hence it is not possible to use this method to add multiple command outputs to a single file. Instead, we can use `>>` to append these outputs to the file. Over here, running `/challenge/run >> ~/the-flag` appends the two half outputs of the `/challenge/run` command to the `the-flag` file. If we do not use `>>`, then only the second half would get stored in the file. After this, we can execute `cat ~/the-flag` to read the flag.


```
acker@piping~appending-output:~$ /challenge/run >> ~/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat ~/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{EY07vJn2tho-dFDOUjznHkhEu7W.QX3ATO0wCMxAzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```


## What I Learned
I learnt how we can redirect the output of multiple commands to a single file using the `>>` character to append these inputs instead of simply redirecting them.

## References
None.