# Split-Piping stderr And stdout
The challenge asks you to open the terminal in the pwn.college DOJO and write a command to split pipe stderr and stdout.

## My Solve
**Flag:** `pwn.college{AQoE-5sFS1GWeGNQ9wnbugSXe3N.QXxQDM2wCMxAzNzEzW}`

In this challenge, we put all the information we have gained in this module to use. We are given a `/challenge/hack` program, and `/challenge/the` which is meant to store the redirected errors (stderr), and `/challenge/planet`, which is meant to store the redirected output (stdout). If we wish to send both stderr and stdout differently, then we cannot use `2>& 1` like we previously did, as that merges the two into one file. Instead, we must execute the command `/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)` if we want to get the flag in return. Over here, the command output from hack gets sent to the program `planet`, which is treated as a named pipe, or a termporary file due to Process Substitution, and hence we can redirect output to it using just the `>` character. At the same time, we use `2>` to redirect stderr to the temporary file created by the `the` program.


```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{AQoE-5sFS1GWeGNQ9wnbugSXe3N.QXxQDM2wCMxAzNzEzW}
```


## What I Learned
In this challenge I was able to put to use all the skills I have learnt in this module so far in order to execute a redirection technique.

## References
None.