# Implicit Relative Paths
The challenge asks you to open the terminal in the pwn.college DOJO and move back to the root directory and invoke the run program with a relative path.

## My Solve
**Flag:** `pwn.college{MXAw5EWOPcuaKn_S5j8ir7xDblr.QX5QTN0wCMxAzNzEzW}`

In this challenge, we make the use of relative paths. The program starts out with `/c` as the **cwd** (Current Working Directory) of the terminal process, meaning that any command we enter, will be invoked within the `/c` directory. But we need to access `/challenge/run` which is in the root directory. So we cd to the root directory using `cd /`. Now, since we are already in the root directory and know that `/challenge/run` is located within this very folder, we can omit the '/' from the beginning of the path to turn it into a relative path.

```
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MXAw5EWOPcuaKn_S5j8ir7xDblr.QX5QTN0wCMxAzNzEzW}
```
## What I Learned
I learnt about relative paths in linux, which are arguments that allow you to access sub-directories and the programs within the current working directory or `cwd` of the terminal process, without needing to start the path's location from the root directory. This allows us to write shorter arguments, instead of having to write the absolute path all the way from the root whenever we wish to access any program or sub-directory.

## References
None.