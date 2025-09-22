# Position Elsewhere
The challenge asks you to open the terminal in the pwn.college DOJO and move to an entirely different path to access the `run` program and get the flag.

## My Solve
**Flag:** `pwn.college{w72Ii0rtZxxG6dEHTknQwXppqeL.QX3QTN0wCMxAzNzEzW}`

This challenge is an extension of the 'Position_thy_Self' challenge where we put our newly learned knowledge of the `cd` command to use in order to change the directory to `/usr/share/build-essential` so that we can invoke `/challenge/run` program in order to get the flag.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/build-essential
hacker@paths~position-elsewhere:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{w72Ii0rtZxxG6dEHTknQwXppqeL.QX3QTN0wCMxAzNzEzW}
```
## What I Learned
I was able to further apply my knowledge of the `cd` command to access a deeper sub-directory in order to get the flag.

## References
None.