# Position Yet Elsewhere
The challenge asks you to open the terminal in the pwn.college DOJO and move to an entirely different path to access the `run` program and get the flag.

## My Solve
**Flag:** `pwn.college{QfS62-Q4kPM7lKjoyFtoWqaC29D.QX4QTN0wCMxAzNzEzW}`

This challenge is once again an application of the `/cd` command that we learned in earlier challenges. To access the `/challenge/run` program, we must `cd` or change our directory to the `/usr/share/doc` directory so that the program can be invoked with its absolute path.

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-yet-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{QfS62-Q4kPM7lKjoyFtoWqaC29D.QX4QTN0wCMxAzNzEzW}
```
## What I Learned
I was able to once again test my knowledge of the `cd` command to access multiple sub-directories in the `/usr` directory in root in order to get the flag.

## References
None.