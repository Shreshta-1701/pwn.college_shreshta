# Program and Absolute Paths
The challenge asks you to open the terminal in the pwn.college DOJO and find the flag by accessing the `run` program in the `challenge` directory.

## My Solve
**Flag:** `pwn.college{sOYsrE1b1o3euJa1509bGfUIIrw.QX1QTN0wCMxAzNzEzW}`

In this program, we learn how to access programs that are in another sub-directory of the root directory. We can access the `/run` program (a program inside the challenge directory) which holds the flag for this challenge. To do so, we need to enter `/challenge/run` in the terminal. `/challenge` enters the challenge directory from the root, and then `/run` accesses the 'run' program in the challenge directory.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{sOYsrE1b1o3euJa1509bGfUIIrw.QX1QTN0wCMxAzNzEzW}
```
## What I Learned
I learnt about sub-directories in Linux and how we can access programs that are located further into the system.

## References
None.