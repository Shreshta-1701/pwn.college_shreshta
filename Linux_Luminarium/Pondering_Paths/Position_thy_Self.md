# Position Thy Self
The challenge asks you to open the terminal in the pwn.college DOJO and change the directory to `/tmp` to access the `run` program and get the flag.

## My Solve
**Flag:** `pwn.college{IEppwaMnYpiRQJt6MUWzBVVLq-l.QX2QTN0wCMxAzNzEzW}`

In this program, we learn how to change the current working directory of the terminal. We can access the `/run` program (a program inside the challenge directory) which holds the flag for this challenge. But this `/challenge` directory lies in a `/tmp` folder. Hence, to invoke `/challenge/run` we first need to `cd (Change Directory)` to `/tmp`. Then we will be able to access the challenge sub-directory.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /tmp
hacker@paths~position-thy-self:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{IEppwaMnYpiRQJt6MUWzBVVLq-l.QX2QTN0wCMxAzNzEzW}
```
## What I Learned
I learnt about how we can change the current directory that the terminal operates in using the cd command with a single argument, the argument being the directory we want to move over to. I also learnt how absolute paths work when you are in a folder other than / (root).

## References
None.