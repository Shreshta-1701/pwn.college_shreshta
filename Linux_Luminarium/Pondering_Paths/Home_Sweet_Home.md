# Home Sweet Home
The challenge asks you to open the terminal in the pwn.college DOJO and copy the contents of `/challenge/run` to another directory with some pre-defined constraints.

## My Solve
**Flag:** `pwn.college{MPo7A_KMV9b6rEwJoZSIFB2R2Us.QXzMDO0wCMxAzNzEzW}`

For the `hacker` user, the default directory in which the terminal opens is the `/home/hacker` directory, which also has a shorthand version that is `~`, something which is identified by bash. Whenever bash sees ~ in a way similar to how it would be used in a path, it expands the shorthand to `/home/hacker`, which is the default cwd. The program asks us to copy the flag and write it into another directory using the `/challenge/run` command with an argument containing the path where it needs to be copied. But this new path must be absolute, must be within the home directory, and must be smaller than or equal to 3 characters when not expanded. In order to fulfill these conditions, we can simply copy the contents into the `/home/hacker` or the default directory. Hence, we can use `~/~` as an argument to `/challenge/run`, which copies the contents of `/challenge/run` into `/home/hacker/~` and gives us the flag. The second ~ is not expanded into /challenge/run as only the leading ~ will expand in such scenarios. We could also use any random character instead of the second ~, and it would give us the same result, as long as we are within the constraints.

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/~
Writing the file to /home/hacker/~!
... and reading it back to you:
pwn.college{MPo7A_KMV9b6rEwJoZSIFB2R2Us.QXzMDO0wCMxAzNzEzW}
```
## What I Learned
I learnt about how the default cwd of the terminal that we will be operating on throughout the course is actually the `/home/hacker` directory and I was able to put to use all of the knowledge that I have gained in this module in order to copy the contents of `/challenge/run` to a new path that was within the predefined constraints set by the challenge.

## References
None.