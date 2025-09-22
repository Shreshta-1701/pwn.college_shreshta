# Implicit Relative Path
The challenge asks you to open the terminal in the pwn.college DOJO and move to the `/challenge` directory and use `./` in order to access the run program directly.

## My Solve
**Flag:** `pwn.college{E_rZsven_KvG1AlU5tcDsG60CAx.QXxUTN0wCMxAzNzEzW}`

Linux does not allow you to run programs in the **cwd** by simply entering their names. This is a security measure to prevent the system from accidentally executing core system utilities with the same name when you enter the name of the program you want to run within the same directory. However, we can bypass this restriction with the help of `./`. This essentially refers to the same directory, and hence we can use `./` to access only the program within the challenge directory. So first, we cd into the challenge directory, and to directly invoke the `run` program in the cwd, we enter `./run` in the terminal, which searches for the `run` program in the same directory (As . refers to challenge) and runs it, to give us the flag.

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{E_rZsven_KvG1AlU5tcDsG60CAx.QXxUTN0wCMxAzNzEzW}
```
## What I Learned
I learnt about how we can use the `./` argument to invoke programs within the cwd without having to write the absolute path of the program, and without having to worry about the system executing other programs with the same name, as now we have specified that we only wish to execute the `run` program in the current directory.

## References
None.