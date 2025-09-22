# Explicit Relative Paths
The challenge asks you to open the terminal in the pwn.college DOJO and move back to the root directory but use `.` to access the contents of the directory.

## My Solve
**Flag:** `pwn.college{0Y69tRIROVr2YPbb-20ag9YQDAf.QXwUTN0wCMxAzNzEzW}`

In this challenge, we make the use of explicit relative paths. The program starts out in a different directory, from where we need to access the root directory and then invoke the `/challenge/run` command. To turn this into an explicit path, we can use `.`. A single dot refers to the same directory. For example - `/challenge/.` still refers to the challenge directory. If we access `.` from the root directory, it would be the same as accessing the root directory itself. Hence, the command `./challenge/run` translates to the absolute path `/challenge/run`, starting from the root in this case as the root is the current working directory after we cd into it.

```
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0Y69tRIROVr2YPbb-20ag9YQDAf.QXwUTN0wCMxAzNzEzW}
```
## What I Learned
I learnt about explicit paths in Linux and how we can further shorten arguments by using dots to refer to the same directory. Using multiple dots would allow us to access parent directories. Every dot added to the first goes back by one directory.

## References
None.